//C3/Tìm số chẵn , số lẻ
 private void btn_giai_Click(object sender, EventArgs e)
 {
     int n;
     n = Convert.ToInt32(txt_N.Text);
     for(int i=0;i<n;i++)
     {
         if (i % 2 == 0) txt_sochan.Text += i.ToString() + " ";
         else
         {
             txt_sole.Text+=i.ToString() + " ";
         }
     }
 }