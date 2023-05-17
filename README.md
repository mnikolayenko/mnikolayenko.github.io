# mnikolayenko.github.io

<html lang="en">
    <head>
        <meta charset="utf-8">
    </head>
    <body>
        <canvas id="canvasOne" width="1024" height="768">
            Your browser does not support HTML5 Canvas.
        </canvas>
        <script 
        src="https://files.worldwind.arc.nasa.gov/artifactory/web/0.9.0/worldwind.min.js"
        type="text/javascript"></script>
        <script type="text/javascript">
            var wwd = new WorldWind.WorldWindow("canvasOne");
            wwd.navigator.range = 20000000; // zoom out to see the entire country

            var layer = new WorldWind.RenderableLayer("Kazakhstan Border");

            var borderFile = "https://www.ngdc.noaa.gov/mgg/shapefiles/world/nation/kz.shp";
            var borderConfig = {
                shapeFile: borderFile,
                style: {
                    fillColor: WorldWind.Color.WHITE,
                    outlineColor: WorldWind.Color.BLACK,
                    outlineWidth: 1
                }
            };
            var borderShape = new WorldWind.Shapefile(borderConfig);
            layer.addRenderable(borderShape);

            wwd.addLayer(layer);
        </script>
    </body>
</html>



[![](https://mermaid.ink/img/pako:eNqtWG1P21YU_iuWK022lESJHQjxpEplBakf-mn9VOVLRsKIGhIUglqGkCiIoYl2MEAjQkAI2z5WopRQSMH8het_tOee67w7jnMpEYlzfV6e85x7zj3OijpTzGRVS53NF9_OzKVLZeXVZKqwWF7OZxV2xGx2xx7YBbtnN86OMpvL560n00n-Ci2WS8U3WeuJaZrudfhtLlOes4yFdz-2TOyzA1dtIvHT1NRkQLV_W2rJ6NRUMhpQrdJSm55-Fk08C6h2xM5bas8T0aDedtk_rCpDyqEs0BN2zk5l-KzIxrgP1apMKnbZiYTa5IuXMuGdAOepTHgn7JReNTnlc_afrN9dVpNT3YdqVYakMyieySkesb9lFY_l8nmKOKsAfCCbVVc9Enuk_4jxWAOmvAFsEbYnzwCpP4YBYcB4rAFpBj7BQE02flKWj16oS8Zeg7pkYyBVWdhCeTTQUF_65ddSemFOSam9Z35KTRUU_PGDXNM0fNRxo-6sQeCb84HdO9vsVmFXkF3DrYazzmxnTdf1tlo4HH7KD3QNbzdQhmXnPbxceqt2Kj7lB6XGKpB_gMY3wrQOYR_XPY5x7mkUFJw6G1wRchzCus5D57Kd4XtCtKFyxb022SAPCEl8yxYyXqZO2IWz4WzBnB3moJ1Ngr-Fq_esAT-3inCChXVFo-Okpne5AHhfFzSBdGlUBG2HgrhDRHLH_cF_izgFl558YuULs_sYZRe68oM7e2gU1VYz-QiioXjE5hpq8eaaqIhs7GHpCtT80eTgAWq_4wuscmxgg8Nz5fV2dJ2hn3sS6p0qYobwt9c6GO01XUNwG-yafWYXyotXfYYq7bS4hpqXvrmqgkkbIL8i4Tbi5zm5pGrixNcpZCzzwvrqslYnhutdCT5sppgmM018ELuYuDS8XYqstSnh2_kKNtvF0QvtL-dPDs6d9viW7HIpZkDhYSCBLWAY4TT8h_nG460Cvq95wxjg-7SZMD77dbrlX4c6E5Of167kOxBB3XvtRW8k-0LBr-TJWyBU7ljpiawDiiLEhnIjxHqwuD4C4aFJ1bd6eTvgXPlWsX8t9pu48eOSMAVCT8OyJ5d0ZwCsXVTBptvg0MvQcdZEM0bpiWLsPUv8ugd5EoW3KwoPH_pgMRq3NXaGVtKgLm9TY2014S9At4Gif3C2eRhnPaa6dmZTlG8YiPahI1_da8TmYGyY6HkIyCmQiei9GzEEgyKDqAcyvjoasuOgyI6DIzv2RHbsg8y3uN3Zfnh5QxDnLc_awfAi7xD22IAtrz0gIrEgR6oe3J7xne2ZI9obwjw9UwRhvhbifXNvOO_oWHTy2l5jmrMpxjSbNtS1eyjfhoQ7G5G4B7WzQ8mjM53PW0C2QzHeDEgmBdITF09msJYBYdg-0oObNoLU1Qj2zBHt-eaVHreGZ_UT1moBDkznI6WlQZ2-O5tIEq457s8ihXxGd7ZFnuvE9m3fSUvwurCOXHaD7Bjfrzzo8c-TRLqjD5p37yhuOhs_0ta7p6fAgOc42e4AIMNMn41HsOJe4kMNqfPZ0nw6l1EtdYXfTanluex8NqVauMykS294LKuQSy-Viz8vF2ZUazadX8yG1KWFTLqcfZ5Lg6f51upCuqBaK-o71TLi8chYPDkRTYwlk4mx-Hg8pC6rVsKMjI1HjagZN5KJmGEaqyH1t2IRFqKRiYkJMx6LjicNIxZPjo-Tudd0s1xagvVsJlcull6Kn-Tpl_nV_wHomC3w?type=png)](https://mermaid.live/edit#pako:eNqtWG1P21YU_iuWK022lESJHQjxpEplBakf-mn9VOVLRsKIGhIUglqGkCiIoYl2MEAjQkAI2z5WopRQSMH8het_tOee67w7jnMpEYlzfV6e85x7zj3OijpTzGRVS53NF9_OzKVLZeXVZKqwWF7OZxV2xGx2xx7YBbtnN86OMpvL560n00n-Ci2WS8U3WeuJaZrudfhtLlOes4yFdz-2TOyzA1dtIvHT1NRkQLV_W2rJ6NRUMhpQrdJSm55-Fk08C6h2xM5bas8T0aDedtk_rCpDyqEs0BN2zk5l-KzIxrgP1apMKnbZiYTa5IuXMuGdAOepTHgn7JReNTnlc_afrN9dVpNT3YdqVYakMyieySkesb9lFY_l8nmKOKsAfCCbVVc9Enuk_4jxWAOmvAFsEbYnzwCpP4YBYcB4rAFpBj7BQE02flKWj16oS8Zeg7pkYyBVWdhCeTTQUF_65ddSemFOSam9Z35KTRUU_PGDXNM0fNRxo-6sQeCb84HdO9vsVmFXkF3DrYazzmxnTdf1tlo4HH7KD3QNbzdQhmXnPbxceqt2Kj7lB6XGKpB_gMY3wrQOYR_XPY5x7mkUFJw6G1wRchzCus5D57Kd4XtCtKFyxb022SAPCEl8yxYyXqZO2IWz4WzBnB3moJ1Ngr-Fq_esAT-3inCChXVFo-Okpne5AHhfFzSBdGlUBG2HgrhDRHLH_cF_izgFl558YuULs_sYZRe68oM7e2gU1VYz-QiioXjE5hpq8eaaqIhs7GHpCtT80eTgAWq_4wuscmxgg8Nz5fV2dJ2hn3sS6p0qYobwt9c6GO01XUNwG-yafWYXyotXfYYq7bS4hpqXvrmqgkkbIL8i4Tbi5zm5pGrixNcpZCzzwvrqslYnhutdCT5sppgmM018ELuYuDS8XYqstSnh2_kKNtvF0QvtL-dPDs6d9viW7HIpZkDhYSCBLWAY4TT8h_nG460Cvq95wxjg-7SZMD77dbrlX4c6E5Of167kOxBB3XvtRW8k-0LBr-TJWyBU7ljpiawDiiLEhnIjxHqwuD4C4aFJ1bd6eTvgXPlWsX8t9pu48eOSMAVCT8OyJ5d0ZwCsXVTBptvg0MvQcdZEM0bpiWLsPUv8ugd5EoW3KwoPH_pgMRq3NXaGVtKgLm9TY2014S9At4Gif3C2eRhnPaa6dmZTlG8YiPahI1_da8TmYGyY6HkIyCmQiei9GzEEgyKDqAcyvjoasuOgyI6DIzv2RHbsg8y3uN3Zfnh5QxDnLc_awfAi7xD22IAtrz0gIrEgR6oe3J7xne2ZI9obwjw9UwRhvhbifXNvOO_oWHTy2l5jmrMpxjSbNtS1eyjfhoQ7G5G4B7WzQ8mjM53PW0C2QzHeDEgmBdITF09msJYBYdg-0oObNoLU1Qj2zBHt-eaVHreGZ_UT1moBDkznI6WlQZ2-O5tIEq457s8ihXxGd7ZFnuvE9m3fSUvwurCOXHaD7Bjfrzzo8c-TRLqjD5p37yhuOhs_0ta7p6fAgOc42e4AIMNMn41HsOJe4kMNqfPZ0nw6l1EtdYXfTanluex8NqVauMykS294LKuQSy-Viz8vF2ZUazadX8yG1KWFTLqcfZ5Lg6f51upCuqBaK-o71TLi8chYPDkRTYwlk4mx-Hg8pC6rVsKMjI1HjagZN5KJmGEaqyH1t2IRFqKRiYkJMx6LjicNIxZPjo-Tudd0s1xagvVsJlcull6Kn-Tpl_nV_wHomC3w)