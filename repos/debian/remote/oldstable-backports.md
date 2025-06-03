## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:721eee78d14d030912669fac06e1147bb4c0dbc6d61b3e64a30325a97c756c23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:23348b4376b0a4066763219214bb06da475e25dd7d81d5afc4abdaae2faf9dfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53750419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede3b68fc019acfcbc603b065801643e9eb3835fa837163008d2e85ec0bbb8aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1b5ead8b01d563e8daf7f2e0d35b5b01de195b353783c416faaa75e8856c6605`  
		Last Modified: Tue, 03 Jun 2025 13:37:17 GMT  
		Size: 53.8 MB (53750197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee797bf36c199e7e588509bfb98e0660cb77700cb784c92d8682211cbbbfbff9`  
		Last Modified: Tue, 03 Jun 2025 19:51:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8af8ddd24854c21d31d2fe1a9bd03c976372b904358897a503b1e2fdc5ab534e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49244d9e44807c8affcc70dd5e1247bed823d9b6aa3434874706d72540fa40d4`

```dockerfile
```

-	Layers:
	-	`sha256:8fe2e494335bd30d92eae0ef2b3e5a470ffdb030a2f53426ed08032b88cf5aa0`  
		Last Modified: Tue, 03 Jun 2025 21:25:14 GMT  
		Size: 3.9 MB (3938726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff32ac2b8971f3a4bbd287d8c7cf4574e1ef3c7d62623891a5781dc24e23ea06`  
		Last Modified: Tue, 03 Jun 2025 21:25:16 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:910c7fc680ae08d5386d1e550b7dddfdea491d63ed755696437191a3ec534964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49042214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40047090b1a042908886f851b6fb75553e6bf3a426c6089a2c2ece387e144539`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:97e55dacf5fd10f20023b06b7c48447024cf7ff20e3947f2f9464d1938040aae`  
		Last Modified: Tue, 03 Jun 2025 19:13:36 GMT  
		Size: 49.0 MB (49041990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e945739e88889cf8189400120ccc98be4f0b7125210139d574a820d6773c19ab`  
		Last Modified: Wed, 21 May 2025 23:12:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8c0f124a76872b1982831d4aaa872763b3c29bdcd5396bb4bf342ff29bcc7e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21b705f37c7d9e382d54148b5fafeedcfac080382693a7768f390224491798f`

```dockerfile
```

-	Layers:
	-	`sha256:03fdd5abffca6f194d377b717d1227105e4d9cad4dc8bd24dd72a86e542129d0`  
		Last Modified: Wed, 21 May 2025 23:12:40 GMT  
		Size: 3.9 MB (3940288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e213467dc7e1f228465c7825fe01297c4be78ba3410cf7480c83e5cca49021`  
		Last Modified: Wed, 21 May 2025 23:12:39 GMT  
		Size: 5.9 KB (5904 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6d1c1cd65834bcbdba264b52b5487825c123b029fd8c4941da4020a5e907436c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162a6d35a172758dd48dca0ad3331c5689ac249c8abf7a8a7a0fc792443afca6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b6fd334f2968041f40df572e77da0fcdcd6993f8f410402d305550f66cb48722`  
		Last Modified: Tue, 03 Jun 2025 19:02:07 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cefcf5adf5e424b08ab3962d8a5595b534e9dce4818f88b557339847030a32f`  
		Last Modified: Wed, 21 May 2025 23:12:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ae302d2c0cd50f2e4aabf96b96a43d6dd565fd1962badc8d3c57c9f70a439fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566f2e4dbc539ca05d0d302fad9e75e41223826d2844e587896e777db64e682b`

```dockerfile
```

-	Layers:
	-	`sha256:8c026c694262889b31916a200e073003c7c6cf12ed5a10b4e48890cbfa8eb83e`  
		Last Modified: Wed, 21 May 2025 23:12:11 GMT  
		Size: 3.9 MB (3938306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c5342394fec1f9d1112ba438b46a3c4bbfe29ec6ffd3efcbece17dc56db212`  
		Last Modified: Wed, 21 May 2025 23:12:10 GMT  
		Size: 5.9 KB (5919 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5cad2df2c8f39da529497d620007cf66b035654419ae496168af394ae699680e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54686004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb598145b47d11dc14043a81780d377fd7e4a0e5679b0e918ca44dd94ab8b5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d38b364b671b52c8fb1f3ba35872a93aff8e868b054baffb72f7589a2aa1a0c6`  
		Last Modified: Wed, 21 May 2025 22:28:07 GMT  
		Size: 54.7 MB (54685779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f142d3063e4092b02e5c1896d98bf0b2244f3700894d07b83ac669e2ff7248db`  
		Last Modified: Wed, 21 May 2025 23:11:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:52b91692d3f5f8a582ac03dc7c4cd14f2d0bed63d26a8974ece75a07cad2a8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f85fd4356e45584275aa2b6f2098d5f1fd2b59ba0192d460d77f68f8c799b70`

```dockerfile
```

-	Layers:
	-	`sha256:9202c8b668f213c16a88cea25cc1c68491d9c1fef1b9855d09475192397e3918`  
		Last Modified: Wed, 21 May 2025 23:11:50 GMT  
		Size: 3.9 MB (3935280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd77e9b5be1d801b1c5ed0dc066273a19db74e371a276db12e8bf220f1d3ebb0`  
		Last Modified: Wed, 21 May 2025 23:11:50 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
