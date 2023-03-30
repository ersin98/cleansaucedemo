* pytest.mark:
* Test işlemlerinde meta veriler eklemeye yarar.
# @pytest.mark.parametrize
	@pytest.mark.parametrize("x,y", [(1, 2), (3, 4)])
- Aynı testi farklı parametreler ile yapmaya yarar. Parametre adları ve değerleri bağımsız değişkenler olabilir.
#	@pytest.mark.usefixtures
	@pytest.mark.usefixtures("some_fixture")
- Bir ya da birden fazla fixture için açıkça argüman olarak iletmeden kullanmaya yarar.
# @pytest.mark.skipif
	@pytest.mark.skipif(sys.version_info < (3, 6), reason="requires python3.6 or higher")
- Belirli bir koşul sağlandığında testi veya sınıfı atlamaya yarar. Koşul bağımsız değişken olabilir.
# @pytest.mark.skip
	@pytest.mark.skip(reason="pass")
- Koşulsuz olarak atlamaya yarar. 
# @pytest.mark.xfail
	@pytest.xfail(reason="bug")
	@pytest.xfail(strict=True)
	@pytest.xfail(run=False)
- Testin hatalı olmasının beklediğini söyler.
- reason = Hatannın sebebini açıklar.
- strict = Parametre testlerinin daha sıkı kontrol edilmesini sağlar. Test edilmek isteden davarınışın gerçekten test ediliğinden emin olunmak için kullanılır. 
- run = Çalıştırılmasını engeller. Özellikle yorumlayıcıyı çökerten xfailing testlerine kullanışlıdır.
