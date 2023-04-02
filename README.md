# plateau-bldg-lod1-pmtiles

## データについて
- 本データは、国土交通省がオープンデータとして公開している、[3D都市モデルPLATEAUの建築物データ（LOD1）](https://www.geospatial.jp/ckan/dataset/plateau)を[tippecanoe](https://github.com/felt/tippecanoe)で[PMTiles形式](https://github.com/protomaps/PMTiles)に変換したデータになります。
- オープンソースソフトウェアで構築

## デモサイト
- https://web-map-maplibre.s3.ap-northeast-1.amazonaws.com/PLATEAU-VIEW/index.html
- サンプル画像
![image](https://user-images.githubusercontent.com/71203808/229335162-f3279b0a-b435-494d-bda5-bf7d797965f6.png)

## データ配布
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/maff-fude/fude_2022_01_47_centroid.pmtiles`(1.2GB)
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/maff-fude/fude_2022_01_47.pmtiles`(19.5GB)

## ベクトルタイル設計情報
### ■ 重心(fude_2022_01_47_centroid.pmtiles)
- 筆ポリゴンがある位置を小縮尺でも把握できるようにするための重心データです。
- tippecanoeによるデータの間引きを行っていません。

#### ズームレベル範囲
2-13

#### 属性
属性は全て外してあります。

### ■ 筆界(fude_2022_01_47.pmtiles)
- 筆ポリゴンそのものを可能な限り生かしたデータです。
- tippecanoeによるデータの間引きを行っていません。

#### ズームレベル範囲
12-16

#### 属性
- 筆ポリゴンの属性はそのまま生かしています（前前年筆ポリゴンID以外）。
- 結果として、次の属性がついていると認識しています。

- 属性項目名 名称
- polygon_uuid 筆ポリゴンID
- land_type 耕地の種類
- issue_year 公開年度
- edit_year 調製年度
- history 履歴
- last_polygon_uuid 前年筆ポリゴンID
- local_government_cd 地方公共団体コード
- point_lng 重心点座標（経度）
- point_lat 重心点座標（経度）

## PMTiles Viewer
- PMTilesはPMTiles Viewerで閲覧することができます。
- https://protomaps.github.io/PMTiles/

## ライセンス
本データセットは[CC-BY-4.0](https://github.com/shi-works/Maff-FudePolygon-PMTiles/blob/main/LICENSE)で提供されます。使用の際には本レポジトリへのリンクを提示してください。

また、本データセットは農水省がオープンデータとして公開している、筆ポリゴン（2022年度公開）を加工して作成したものです。本データセットの使用・加工にあたっては、[筆ポリゴンの利用規約等](https://www.maff.go.jp/j/tokei/porigon/)を必ずご確認ください。
