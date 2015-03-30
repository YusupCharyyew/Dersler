SQL VeriTabanına Veri Ekleme

veritabanına baglanma

```a
SqlConnection Baglanti = new SqlConnection();
Baglanti.ConnectionString=@"Data Source=.\SqlExpress; Initial Catalog = VeriTaban Adı; Integrated Security = True;";
```
```c
SqlCommand Komut = new SqlCommand();
Komut.CommandText = @"Insert Into Tablo Adi (AlanAdi, AlanAdi) Values (@Ad, @Soyad)";

Komut.Parameters.AddWithValue("@Ad", textBox1.Text);
Komut.Parameters.AddWithValue("@Soyad", textBox2.Text);

Baglanti.Open();
Komut.ExecuteNonQuery();
Baglanti.CLose();

MessageBox.Show("Kişi bilgileri kaydedildi");
```

