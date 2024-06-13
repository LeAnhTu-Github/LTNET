
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