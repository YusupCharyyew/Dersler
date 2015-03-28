```c
SqlConnection Baglanti = new SqlConnection();
Baglanti.ConnectionString = @"Data Source=.\SqlExpress; Initial Catalog=dbOkul; Integrated Security=true";

SqlCommand komut = new SqlCommand();
komut.CommandText = "INSERT INTO Ogrenci VALUES ('321','Mark','Zuck')";

Baglanti.Open();
komut.ExecuteNonQuery();
Baglanti.Close();
```