## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:0141fccdcc543d5707f9ccbc160ee8c3535f96716869ca72582797017bca184d
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
$ docker pull rethinkdb@sha256:b03b73e4197d2085758a3de6ffa8b96b2c762977a57074d2b647d03a6525fe95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48909164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687979a0f67e726971e947a4f5713ab8983ae59a664df87b8fcfdfe7057c0f2a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14e32101e30c2e5120dc94feec5baf8794a155b620f500de222b32cf2e2cadb`  
		Last Modified: Tue, 23 Jul 2024 07:16:11 GMT  
		Size: 9.8 MB (9787378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8999edeec91d8564c1e8867090f7265aded1df664eb6e3a5a7f155ba241d67d6`  
		Last Modified: Tue, 23 Jul 2024 07:16:11 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00c634f16aa8055968ca08a4e100aa71955d2e57f72104a53fd7cefe21d0fdd`  
		Last Modified: Tue, 23 Jul 2024 07:16:11 GMT  
		Size: 10.0 MB (9992736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b5f04a602bd4a7a93cba5a1ed3ef87b9fa7d8dbd60c814a9923778a5792be`  
		Last Modified: Tue, 23 Jul 2024 07:16:11 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:1544f46e95b4290dfa8fb5dc26bb577fecd6ec05a0561f37abe72502efecc8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16723af6771eba7c04c5b60a15d9654d50b8b70f69d24675d75a3457d47b80d`

```dockerfile
```

-	Layers:
	-	`sha256:7b5ebeb456e0f2d215ce9107cfbebe1808ebd6c6c1ff9b1e3cfe7ad87fc722be`  
		Last Modified: Tue, 23 Jul 2024 07:16:11 GMT  
		Size: 2.6 MB (2613189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cdb5208e1a224deb6700d664678ff207c92e153d0251e16367b995c6b97371`  
		Last Modified: Tue, 23 Jul 2024 07:16:11 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:8ee96586a55046fac4f008da27a266c3f89a7ab12b907961b6848712938e6294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48108208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280f761067d918af9915b290ac2c7c0f12225adefbd64216297c31a6655ba987`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d60a6d6f67af93e64496598e86cda5a9eee1756fe6a18efaa6f28f9b23d748`  
		Last Modified: Wed, 24 Jul 2024 07:15:27 GMT  
		Size: 9.6 MB (9586400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d06c6cdc1f2d9a3efef47fbe086378e6dffb9a496acc09f6414c1c1d408db7`  
		Last Modified: Wed, 24 Jul 2024 07:15:26 GMT  
		Size: 2.7 KB (2674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a384205f363746859e96434c1009051cfcdd1ad9e526cea6d85e4f56326380c`  
		Last Modified: Wed, 24 Jul 2024 07:15:27 GMT  
		Size: 9.4 MB (9362471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b870999b20d2c616b698d5ba2cfcb7ae84bfd40339555502785afa49bc805a`  
		Last Modified: Wed, 24 Jul 2024 07:15:26 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4011a18667ad4030eda9a9b5ace94746a3562b8e73b1d771969efbce90014abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fd7996e7d69f58a1e972d271c43f6c3f439381d0f7d0f9012a9c9c64d1fe60`

```dockerfile
```

-	Layers:
	-	`sha256:253e3166e1fd4746a299352b3438656aacd2367e457bd3174508dec5444c1236`  
		Last Modified: Wed, 24 Jul 2024 07:15:27 GMT  
		Size: 2.6 MB (2613523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e089724ea46873db2b1223b8edf0281f8d777e76948cf65db7550f38d077a99`  
		Last Modified: Wed, 24 Jul 2024 07:15:26 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:bd52ca110ec4265493217f4de87aebd32ad0299f55b7a39a93f1630449e0b26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46080915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c901b03dccb26a4024b662af19e35341c738e111cf250a67011fd66c9c1132`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885aa25f5250d735e8008fd8e6488f0cbe1f0d140ed255e7cd768b6c25138ebf`  
		Last Modified: Tue, 02 Jul 2024 10:30:49 GMT  
		Size: 9.3 MB (9284633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66303b9d058d5c456f21416078f03080ef317fc05aa405d559b7c73f03cfac2`  
		Last Modified: Tue, 02 Jul 2024 10:30:48 GMT  
		Size: 2.7 KB (2671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a4874a4c558a3ec6a58f522d05581be88474c1c1a0f5929d4b163115c97328`  
		Last Modified: Tue, 02 Jul 2024 10:30:49 GMT  
		Size: 9.3 MB (9303427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be5130a715b2278698584a5c4782b869d91414c5b8d9a5302c5cfc13027f53c`  
		Last Modified: Tue, 02 Jul 2024 10:30:49 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:44c69a1c68bdbd0390b8e03983e858c93a04b7444da5f011a04638ac574134c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6313e208e4036bca9d13959cd1e6a3679c4c3e72bc7be2742b9933c292b06769`

```dockerfile
```

-	Layers:
	-	`sha256:bd9e970493af7458a30c62fab5bb01d53d0362eb3bd01b766689f8a71efeedaf`  
		Last Modified: Tue, 02 Jul 2024 10:30:49 GMT  
		Size: 2.6 MB (2586135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4f0d6c6b83a727d32e5e7399ed955f1d56cff29d7ee788201bf4e1ffe9a3c33`  
		Last Modified: Tue, 02 Jul 2024 10:30:48 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json
