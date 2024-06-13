



//khai báo 1 mảng 5 phần tử
        private int[] numbers = new int[5];
        // khai báo 1 biến và cấp phát biến ngẫu nhiên
        private Random random = new Random();
        private void button1_Click(object sender, EventArgs e)
        {
            //button nhap
            nhapmang();
            xuatmang();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            //btton thực hiện
            textBox6_TextChanged(sender, e);
            showsum.Text = sum().ToString();
        }
        //Tìm max
        private void textBox6_TextChanged(object sender, EventArgs e)
        {
            int max = numbers[0];
            int index = 0; 
            for (int i = 1; i < numbers.Length; i++)
            {
                if(numbers[i]>max)
                {
                    max = numbers[i];
                    index = i;
                }    
            }  
            showmax.Text = max.ToString();
            showindex.Text = index.ToString();
        }
        //tính tổng
        private int sum()
        {
            int sum = 0;
            for(int i = 0; i < numbers .Length; i++)
            {
                sum += numbers[i];
            }    
            return sum;
        }
        private void nhapmang()
        {
            for( int i = 0; i < numbers.Length; i++ )
            {
                numbers[i] = random.Next(1, 101);
            }    
        }    
        private void xuatmang()
        {
            ar1.Text = numbers[0].ToString();
            ar2.Text = numbers[1].ToString();
            ar3.Text = numbers[2].ToString();
            ar4.Text = numbers[3].ToString();
            ar5.Text = numbers[4].ToString();

        }
//số hoàn hảo
for (int i = 1; i <= a / 2; i++) {
 if (a % i == 0){
 sum += i;
 }
}
if (sum == a) {
 Console.WriteLine("\n{0} là số hoàn hảo.", a);
 } else {
 Console.WriteLine("\n{0} không phải là số hoàn hảo.", a);
 }
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

 private void btn_thoat_Click(object sender, EventArgs e)
 {
     this.Close();
 }
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
//dau cuoi giua tieo
  private void button7_Click(object sender, EventArgs e)//next
  {
      if (k < dt.Rows.Count - 1)
      {
          k = k + 1;
      }
      HienThi(k);
  }

  private void button6_Click(object sender, EventArgs e)//giua
  {
      if (k > 0)
      {
          k = k - 1;
      }
      HienThi(k);
  }

  private void button5_Click(object sender, EventArgs e)//dau
  {
      k = 0;
      HienThi(k);
  }

  private void button8_Click(object sender, EventArgs e)//cuoi
  {
      k = dt.Rows.Count - 1;
      HienThi(k);
  }
//x^2+x=0
    private void btnTinh_Click(object sender, EventArgs e)
    {
        double a = double.Parse(A.Text);
        double b = double.Parse(B.Text);
        double c = double.Parse(C.Text);

        if (a == 0)
        {
            if (b == 0)
            {
                if (c == 0)
                {
                    MessageBox.Show("Phương trình có vô số nghiệm.");
                }
                else
                {
                    MessageBox.Show("Phương trình vô nghiệm.");
                }
            }
            else
            {
                double x = -c / b;
                MessageBox.Show("Phương trình có 1 nghiệm x = " + x);
            }
        }
        else
        {
            double denta = (b * b) - (4 * a * c);
            if (denta > 0)
            {
                double x1 = (-b + Math.Sqrt(denta)) / (2 * a);
                double x2 = (-b - Math.Sqrt(denta)) / (2 * a);
                MessageBox.Show("Phương trình có 2 nghiệm phân biệt:\nx1 = " + x1 + "\nx2 = " + x2);
            }
            else if (denta == 0)
            {
                double x = -b / (2 * a);
                MessageBox.Show("Phương trình có nghiệm kép x = " + x);
            }
            else
            {
                MessageBox.Show("Phương trình vô nghiệm.");
            }
        }
    }

    private void btnThoat_Click(object sender, EventArgs e)
    {
        this.Close();
    }
}
//làm hàm check số chính phương và số nguyên tố
 private bool isprime(int numbers)
 {
     if(numbers < 2) return false;
     for(int i = 2; i < numbers; i++)
     {
         if(numbers%i == 0) return false;
     }    
     return true;
 }
 private bool issquares(int numbers)
 {
     int root = (int)Math.Sqrt(numbers);
     return root*root == numbers;
 }    

 private void button1_Click(object sender, EventArgs e)
 {
     //ok
     int n = Convert.ToInt32(txtN.Text);
     String primeNumbers = "";
     String perfectsquares = "";

     for(int i = 0; i < n; i++)
     {
         if(isprime(i))
         {
             primeNumbers += i + "\t";
         }  
         if(issquares(i))
         {
             perfectsquares += i + "\t";
         }    
     }    
     //gán
     txtSNT.Text = primeNumbers;
     txtSCP.Text = perfectsquares;

 }
 private void btnnew_Click(object sender, EventArgs e)
 {
     //new
     txtN.Text = "";
     txtSCP.Text = "";
     txtSNT.Text = "";
     txtN.Focus();
 }

//làm hàm check số chính phương và số nguyên tố
 private bool isprime(int numbers)
 {
     if(numbers < 2) return false;
     for(int i = 2; i < numbers; i++)
     {
         if(numbers%i == 0) return false;
     }    
     return true;
 }
 private bool issquares(int numbers)
 {
     int root = (int)Math.Sqrt(numbers);
     return root*root == numbers;
 }    

 private void button1_Click(object sender, EventArgs e)
 {

     //ok
     int n = Convert.ToInt32(txtN.Text);
     String primeNumbers = "";
     String perfectsquares = "";

     for(int i = 0; i < n; i++)
     {
         if(isprime(i))
         {
             primeNumbers += i + "\t";
         }  
         if(issquares(i))
         {
             perfectsquares += i + "\t";
         }    
     }    
     //gán
     txtSNT.Text = primeNumbers;
     txtSCP.Text = perfectsquares;

 }

 private void btnclose_Click(object sender, EventArgs e)
 {
     this.Close();
 }

 private void btnnew_Click(object sender, EventArgs e)
 {
     //new
     txtN.Text = "";
     txtSCP.Text = "";
     txtSNT.Text = "";
     txtN.Focus();
 }
//số nguyên tố và số chính phương
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

 private void btntiep_Click(object sender, EventArgs e)
 {
     txta1.Text = "";
     txtb1.Text = "";
     txtc1.Text = "";
     txta2.Text = "";
     txtb2.Text = "";
     txtc2.Text = "";
     showx.Text = "";
     showy.Text = "";

 }

//
//làm hàm check số chính phương và số nguyên tố
 private bool isprime(int numbers)
 {
     if(numbers < 2) return false;
     for(int i = 2; i < numbers; i++)
     {
         if(numbers%i == 0) return false;
     }    
     return true;
 }
 private bool issquares(int numbers)
 {
     int root = (int)Math.Sqrt(numbers);
     return root*root == numbers;
 }    

 private void button1_Click(object sender, EventArgs e)
 {

     //ok
     int n = Convert.ToInt32(txtN.Text);
     String primeNumbers = "";
     String perfectsquares = "";

     for(int i = 0; i < n; i++)
     {
         if(isprime(i))
         {
             primeNumbers += i + "\t";
         }  
         if(issquares(i))
         {
             perfectsquares += i + "\t";
         }    
     }    
     //gán
     txtSNT.Text = primeNumbers;
     txtSCP.Text = perfectsquares;

 }

 private void btnclose_Click(object sender, EventArgs e)
 {
     this.Close();
 }

 private void btnnew_Click(object sender, EventArgs e)
 {
     //new
     txtN.Text = "";
     txtSCP.Text = "";
     txtSNT.Text = "";
     txtN.Focus();
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

 private void btntiep_Click(object sender, EventArgs e)
 {
     txta1.Text = "";
     txtb1.Text = "";
     txtc1.Text = "";
     txta2.Text = "";
     txtb2.Text = "";
     txtc2.Text = "";
     showx.Text = "";
     showy.Text = "";

 }
//khai báo 1 mảng 5 phần tử
        private int[] numbers = new int[5];
        // khai báo 1 biến và cấp phát biến ngẫu nhiên
        private Random random = new Random();
        private void button1_Click(object sender, EventArgs e)
        {
            //button nhap
            nhapmang();
            xuatmang();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            //btton thực hiện
            textBox6_TextChanged(sender, e);
            showsum.Text = sum().ToString();
        }
        //Tìm max
        private void textBox6_TextChanged(object sender, EventArgs e)
        {
            int max = numbers[0];
            int index = 0; 
            for (int i = 1; i < numbers.Length; i++)
            {
                if(numbers[i]>max)
                {
                    max = numbers[i];
                    index = i;
                }    
            }  
            showmax.Text = max.ToString();
            showindex.Text = index.ToString();
        }
        //tính tổng
        private int sum()
        {
            int sum = 0;
            for(int i = 0; i < numbers .Length; i++)
            {
                sum += numbers[i];
            }    
            return sum;
        }
        private void nhapmang()
        {
            for( int i = 0; i < numbers.Length; i++ )
            {
                numbers[i] = random.Next(1, 101);
            }    
        }    
        private void xuatmang()
        {
            ar1.Text = numbers[0].ToString();
            ar2.Text = numbers[1].ToString();
            ar3.Text = numbers[2].ToString();
            ar4.Text = numbers[3].ToString();
            ar5.Text = numbers[4].ToString();

        }
//số hoàn hảo
for (int i = 1; i <= a / 2; i++) {
 if (a % i == 0){
 sum += i;
 }
}
if (sum == a) {
 Console.WriteLine("\n{0} là số hoàn hảo.", a);
 } else {
 Console.WriteLine("\n{0} không phải là số hoàn hảo.", a);
 }
