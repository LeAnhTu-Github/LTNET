
//C4: Giải pt
    private void btn_giai_Click(object sender, EventArgs e)
    {
        float a1, b1, c1, a2, b2, c2;
        a1 = float.Parse(txt_a1.Text);
        b1=float.Parse(txt_b1.Text);
        c1 = float.Parse(txt_c1.Text);
        a2=float.Parse(txt_a2.Text);
        b2=float.Parse(txt_b2.Text);
        c2=float.Parse(txt_c2.Text);

        float D, Dx, Dy, x, y;
        D = a1 * b2 - a2 * b1;
        Dx = c1 * b2 - c2 * b1;
        Dy = a1 * c2 - a2 * c1;

        if(Dx==0)
        {
            if(Dx+Dy==0)
            {
                textBox1.Text = "HPT vo so nghiem";
            }
            else
            {
                textBox1.Text = "HPT vo nghiem";
            }
               
        }
        else
        {
            x = Dx / D;
            y = Dy / D;
            textBox1.Text = "HPT co nghiem x="+x+" \n y="+y+"";

        }
    }
}
private void btngiai_Click(object sender, EventArgs e)
 {
     int a1 = Convert.ToInt32(txta1.Text);
     int b1 = Convert.ToInt32(txtb1.Text);
     int c1 = Convert.ToInt32(txtc1.Text);
     int a2 = Convert.ToInt32(txta2.Text);
     int b2 = Convert.ToInt32(txtb2.Text);
     int c2 = Convert.ToInt32(txtc2.Text);
     //tính hệ pt
     double D = a1 * b2 - a2 * b1;
     double Dx = c1 * b2 - c2 * b1;
     double Dy = a1 * c2 - a2 * c1;
     //dk
     if(D==0)
     {
         if(Dx != 0 || Dy != 0)
         {
             MessageBox.Show("Hệ Phương Trình Vô Nghiệm!");

         }    
         else
         {
             MessageBox.Show("Hệ Phương Trình Vô Số Nghiệm!");
         }

     }    
     else
     {
         showx.Text = (Dx / D).ToString();
         showy.Text = (Dy / D).ToString();
     }    

 }