



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