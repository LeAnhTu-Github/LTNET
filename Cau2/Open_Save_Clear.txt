
//C2: open/save/clear/exit
 private void toolStripMenuItem2_Click(object sender, EventArgs e)
 {
     OpenFileDialog open = new OpenFileDialog();
     open.Filter = "|*.txt";
     if(open.ShowDialog()==DialogResult.OK)
     {
         StreamReader read= new StreamReader(open.FileName);
         richTextBox1.Text = read.ReadToEnd();
         read.Close();
     }
 }

 private void saveToolStripMenuItem_Click(object sender, EventArgs e)
 {
     SaveFileDialog save = new SaveFileDialog();
     save.Filter = "|*.txt";
     if(save.ShowDialog()==DialogResult.OK)
     {
         StreamWriter sw = new StreamWriter(save.FileName);
         sw.Write(richTextBox1.Text);
         sw.Close();
     }
 }

 private void clearToolStripMenuItem_Click(object sender, EventArgs e)
 {
     richTextBox1.Clear();
 }

 private void exitToolStripMenuItem_Click(object sender, EventArgs e)
 {
     this.Close();
 }
