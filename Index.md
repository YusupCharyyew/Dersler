SQL VeriTabanına Veri Ekleme

veritabanına baglanma

```a
SqlConnection Baglanti = new SqlConnection();
Baglanti.ConnectionString=@"Data Source=.\SqlExpress; Initial Catalog = VeriTaban Adı; Integrated Security = True;";
```
-
-Tablo Alanlarına Textbox'daki değerleri kayıt etme
-
-Insert sorgusunda AlanAdlarin ve Degerlaerin sırası önemli. Değerleri AlanAdlarina göre sıralıycas.
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

