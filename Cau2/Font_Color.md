//Câu 2:Font/color 
private void fontToolStripMenuItem_Click(object sender, EventArgs e)
 {
     if(fontDialog1.ShowDialog()==DialogResult.OK)
     {
         richTextBox1.SelectionFont = fontDialog1.Font;
     }
 }

 private void colorToolStripMenuItem_Click(object sender, EventArgs e)
 {
     if(colorDialog1.ShowDialog()==DialogResult.OK)
     {
         richTextBox1.SelectionColor=colorDialog1.Color;
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