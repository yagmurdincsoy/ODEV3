# ODEV3
3. HAFTA ÖDEVİ

/*USA ülkesine ait 2009 yılı içerisinde oluşturulmuş tüm faturaların toplamını
listeleyen sorgu*/

Select SUM(total)
FROM Invoice
WHERE invoice_date IN (2019);


/*Track bilgilerini ait olduğu playlisttrack ve playlist tablolarıyla birleştirme*/

SELECT track_id
FROM PlaylistTrack
INNER JOIN Playlist ON PlaylistTrack.playlist_id = Playlist.playlist_id;


/*Let There Be Rock albümüne ait tüm parçaları listeleyen sanatçı bilgisini içeren ve parça süresi büyükten küçüğe sorgu.*/

SELECT Track, Artist
FROM Track
WHERE Title='Let There Be Rock'
ORDER BY COUNT(milliseconds) DESC;
