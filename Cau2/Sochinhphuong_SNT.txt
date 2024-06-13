
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