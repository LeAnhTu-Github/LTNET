


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