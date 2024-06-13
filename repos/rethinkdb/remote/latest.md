## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:ad827e81409dad91f5838956ac2f3e4bf48003b8283ec9e5f8070fa22d6263e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:ccc55a64a3470f1ccf57a71c68c035a5bb36c855aac5766b1dc7d01fbd37b6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ff2da18d8e79a6c952b67e3a4b916d9458ba54d1f1578761348a1d58d257bd`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["bash"]
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b542a78b7ce69826f9493500db8101702b124f6b50904f7a64d0e10e705862c8`  
		Last Modified: Thu, 16 May 2024 21:17:19 GMT  
		Size: 9.6 MB (9593386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5614ef194174d1e3246e3afe9d6a56f3266c615d13c892ecb1fabeca6766759`  
		Last Modified: Thu, 16 May 2024 21:17:19 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765d3db48d22dce9c4d2d432d01583ef8f95b14bb76f8c2931c7301804f67dc0`  
		Last Modified: Thu, 16 May 2024 21:17:19 GMT  
		Size: 10.0 MB (9992685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7dfb5c68dfcdfbfb654f34a10bed3800088f836a10b6bae96577249ca85332`  
		Last Modified: Thu, 16 May 2024 21:17:19 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:3fb85d53913d3b2c67a9a22df636f72e0db17a43fa2a56adbfa2fd521e3fed9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83830cf7cdb0e8ba1e2ae332b6c825de4309f684250208174d301fda70dcad05`

```dockerfile
```

-	Layers:
	-	`sha256:3bb1d8f47b6d151f12bbe538f890ce6622f050aa816666f1b4eb5da1a0b77ca6`  
		Last Modified: Thu, 16 May 2024 21:17:19 GMT  
		Size: 2.6 MB (2586907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3118f31114fc42e631acb42f59b1eb0ebd5d66f21f6da38d5eb3ca47e46ee018`  
		Last Modified: Thu, 16 May 2024 21:17:19 GMT  
		Size: 13.4 KB (13365 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:0b711c4ece6f1fa3dff966587d04b50b28b6b717b0043c1cd34d1787327aa5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47934921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0081c23c35cc6ceb3eb7da58c9d78731f8d8ceb4604d7ecdb2e7268e70c03dcf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["bash"]
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c31a56eb04b6b65450365135948cbdcab2962b4682e0d14cbb984dd5c080f`  
		Last Modified: Fri, 17 May 2024 00:19:40 GMT  
		Size: 9.4 MB (9390118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefe6e4677697ea0cfc5ea92fbae1351dea0fef52b0237acbd738386164bdeab`  
		Last Modified: Fri, 17 May 2024 00:19:40 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e02e29034ccbd064c52d7bdca792b61938dc9ff30991e89c5da3502684122bb`  
		Last Modified: Fri, 17 May 2024 00:19:40 GMT  
		Size: 9.4 MB (9362538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0216c1e49958429f889932cf199c025ff4c91f3a6e7a32518ad633cddf87c7`  
		Last Modified: Fri, 17 May 2024 00:19:40 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:06d977f6f5f62a6f52d65f4793bb7d66a2d2af7c171bef1024132bfdffa7912c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25701f2d882729455a50d34e8250161bb9de3684ec22c0c6a120a02cf3195e77`

```dockerfile
```

-	Layers:
	-	`sha256:2d5c4e4c56a726af35812c549c6d577be060c147e11c41244fc24644b6af3537`  
		Last Modified: Fri, 17 May 2024 00:19:41 GMT  
		Size: 2.6 MB (2587156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbffc91dc22cc018fcb571637c859b29b3b62d531e17bc6bf781175f58600a9`  
		Last Modified: Fri, 17 May 2024 00:19:40 GMT  
		Size: 13.2 KB (13216 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:bf6dafa1409174edecf8d059a0a8191a93864e8fc215b35bd977a4488bf0eee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45907533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d1cbd417f5435e160eb427c71d362d30572098fde829d07640fe89cb62210f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["bash"]
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9907fb47b35ef72635b3b33b600e3c6f164762908e3143fd83c5a6f6a8b99d`  
		Last Modified: Thu, 13 Jun 2024 12:46:48 GMT  
		Size: 9.1 MB (9088764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998efd1a5f7ad9d8735a4fcec21daaf80fdb9282a91cb0293c9d9ea5e98b1c26`  
		Last Modified: Thu, 13 Jun 2024 12:46:47 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f30a413f1e271fe2abd3e83038e1a4693a24ea40775eca7294a868140516c`  
		Last Modified: Thu, 13 Jun 2024 12:46:48 GMT  
		Size: 9.3 MB (9303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eea02aaa4cf75a710b1454c2ba045a58cbc5d83f5a8c2b7cc37de0bf7ceb1c`  
		Last Modified: Thu, 13 Jun 2024 12:46:47 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:93d74a628a0a7ea4cab33c1486ae2f09031678679b5681fcf3a9087f34bc8ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c8b90b868a93bee08be0cbd6365447866a6b7c3d45ad676d4fe677acd07380`

```dockerfile
```

-	Layers:
	-	`sha256:35674001d4d3320250ae144f4f6b2c19cb62fb5a50e9e1b594fbe6631d87b55f`  
		Last Modified: Thu, 13 Jun 2024 12:46:48 GMT  
		Size: 2.6 MB (2586106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bba25d5827a76a334ed7a298ea38dfebebd86d4cadcc600efaef5e6b14ea612`  
		Last Modified: Thu, 13 Jun 2024 12:46:47 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json
