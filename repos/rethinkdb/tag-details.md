<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-bookworm-slim`](#rethinkdb2-bookworm-slim)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-bookworm-slim`](#rethinkdb24-bookworm-slim)
-	[`rethinkdb:2.4.3`](#rethinkdb243)
-	[`rethinkdb:2.4.4-bookworm-slim`](#rethinkdb244-bookworm-slim)
-	[`rethinkdb:bookworm-slim`](#rethinkdbbookworm-slim)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:97d9fb8de872e30a1a9114c3b9491a4c665bf118f63bbe023a93ba1cd861f40e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d46194ae408e433a09b0ad64935707fd4d2f846a0f1fb39fed6a706a15a59ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898bb84fcf05326892fcfd6db7e48a19975d11ebecfb42ddb7443aff8b425965`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e11538b21c9e2d9ecc355c43addc9a13f176bd157d594cbb79fe48b9df7a7e`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 9.8 MB (9786535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65daa7e1b97965d06f434e1c660d22c523bdec7a69999626680057201cc5b2`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d93caa75dcc0a6337d79936b6408569234a5b28847836d4a5c2fe37e940c06`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 10.0 MB (9992815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ac91b69cbc57d5540e3004cc55a26baa1e99ce806c887a665dd57b7ac5237`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:02a0e1bcc1cfb40728d8cd87e3b7557b293373c6091cca4e3e55bd7fc8d97096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347f8992b84b8c37b4173caf3494ff6eb33e8a9558a16e9bfb0f2f0cf7e21956`

```dockerfile
```

-	Layers:
	-	`sha256:18ac5c2510de93dbb3e2ea858b022cac72864cc49ede34da12e05f3c1e28723b`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 2.6 MB (2586935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d43f7465724b4effcbc5e1c15c96bf19f19887f65709a8e740d6a3859ebee4d`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:7b56d11a281f1e837261d59a15f571be54e8a5aa4b0e875afaf06ef9f17c8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c088906bf631659e01c8743f3efc6ac3ed890eadd759f17557bea4defd57c79a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff3c58159d927eceb79f51c8b36d5a57c533f07869ccba15b528e638dcfc4c`  
		Last Modified: Tue, 02 Jul 2024 23:05:53 GMT  
		Size: 9.6 MB (9586083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aaa396b94a8c2a9ebf6805673d96eaeab110cf9f83ac46992e2834693f2b98`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddb798fede4afbff8c0e74d1d9b6147194e79ba58b0d5094a5cdabd2cad7a9`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 9.4 MB (9362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393536def3696bf836ed6d35f9d03bf67ad0f0d6767da953995bbcf580d3e19d`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b895f110e78c3960769123c3409f90007ba2122836c165e8b2b0d150137f5bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96c1d603c7de21f5be13698ea2adbfd943e6c65ef941d19add4452a3151e12e`

```dockerfile
```

-	Layers:
	-	`sha256:ecffdc790da72d467e322414d265ddaae4ab63b75f1443655bfbd21fd78503ca`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.6 MB (2587269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e2b54664e747ab93a07874a48860339e0050a99773717ba6093ca2b34b8eec`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

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

### `rethinkdb:2` - unknown; unknown

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

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:97d9fb8de872e30a1a9114c3b9491a4c665bf118f63bbe023a93ba1cd861f40e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d46194ae408e433a09b0ad64935707fd4d2f846a0f1fb39fed6a706a15a59ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898bb84fcf05326892fcfd6db7e48a19975d11ebecfb42ddb7443aff8b425965`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e11538b21c9e2d9ecc355c43addc9a13f176bd157d594cbb79fe48b9df7a7e`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 9.8 MB (9786535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65daa7e1b97965d06f434e1c660d22c523bdec7a69999626680057201cc5b2`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d93caa75dcc0a6337d79936b6408569234a5b28847836d4a5c2fe37e940c06`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 10.0 MB (9992815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ac91b69cbc57d5540e3004cc55a26baa1e99ce806c887a665dd57b7ac5237`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:02a0e1bcc1cfb40728d8cd87e3b7557b293373c6091cca4e3e55bd7fc8d97096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347f8992b84b8c37b4173caf3494ff6eb33e8a9558a16e9bfb0f2f0cf7e21956`

```dockerfile
```

-	Layers:
	-	`sha256:18ac5c2510de93dbb3e2ea858b022cac72864cc49ede34da12e05f3c1e28723b`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 2.6 MB (2586935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d43f7465724b4effcbc5e1c15c96bf19f19887f65709a8e740d6a3859ebee4d`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:7b56d11a281f1e837261d59a15f571be54e8a5aa4b0e875afaf06ef9f17c8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c088906bf631659e01c8743f3efc6ac3ed890eadd759f17557bea4defd57c79a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff3c58159d927eceb79f51c8b36d5a57c533f07869ccba15b528e638dcfc4c`  
		Last Modified: Tue, 02 Jul 2024 23:05:53 GMT  
		Size: 9.6 MB (9586083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aaa396b94a8c2a9ebf6805673d96eaeab110cf9f83ac46992e2834693f2b98`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddb798fede4afbff8c0e74d1d9b6147194e79ba58b0d5094a5cdabd2cad7a9`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 9.4 MB (9362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393536def3696bf836ed6d35f9d03bf67ad0f0d6767da953995bbcf580d3e19d`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b895f110e78c3960769123c3409f90007ba2122836c165e8b2b0d150137f5bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96c1d603c7de21f5be13698ea2adbfd943e6c65ef941d19add4452a3151e12e`

```dockerfile
```

-	Layers:
	-	`sha256:ecffdc790da72d467e322414d265ddaae4ab63b75f1443655bfbd21fd78503ca`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.6 MB (2587269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e2b54664e747ab93a07874a48860339e0050a99773717ba6093ca2b34b8eec`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

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

### `rethinkdb:2-bookworm-slim` - unknown; unknown

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

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:97d9fb8de872e30a1a9114c3b9491a4c665bf118f63bbe023a93ba1cd861f40e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d46194ae408e433a09b0ad64935707fd4d2f846a0f1fb39fed6a706a15a59ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898bb84fcf05326892fcfd6db7e48a19975d11ebecfb42ddb7443aff8b425965`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e11538b21c9e2d9ecc355c43addc9a13f176bd157d594cbb79fe48b9df7a7e`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 9.8 MB (9786535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65daa7e1b97965d06f434e1c660d22c523bdec7a69999626680057201cc5b2`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d93caa75dcc0a6337d79936b6408569234a5b28847836d4a5c2fe37e940c06`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 10.0 MB (9992815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ac91b69cbc57d5540e3004cc55a26baa1e99ce806c887a665dd57b7ac5237`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:02a0e1bcc1cfb40728d8cd87e3b7557b293373c6091cca4e3e55bd7fc8d97096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347f8992b84b8c37b4173caf3494ff6eb33e8a9558a16e9bfb0f2f0cf7e21956`

```dockerfile
```

-	Layers:
	-	`sha256:18ac5c2510de93dbb3e2ea858b022cac72864cc49ede34da12e05f3c1e28723b`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 2.6 MB (2586935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d43f7465724b4effcbc5e1c15c96bf19f19887f65709a8e740d6a3859ebee4d`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:7b56d11a281f1e837261d59a15f571be54e8a5aa4b0e875afaf06ef9f17c8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c088906bf631659e01c8743f3efc6ac3ed890eadd759f17557bea4defd57c79a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff3c58159d927eceb79f51c8b36d5a57c533f07869ccba15b528e638dcfc4c`  
		Last Modified: Tue, 02 Jul 2024 23:05:53 GMT  
		Size: 9.6 MB (9586083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aaa396b94a8c2a9ebf6805673d96eaeab110cf9f83ac46992e2834693f2b98`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddb798fede4afbff8c0e74d1d9b6147194e79ba58b0d5094a5cdabd2cad7a9`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 9.4 MB (9362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393536def3696bf836ed6d35f9d03bf67ad0f0d6767da953995bbcf580d3e19d`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b895f110e78c3960769123c3409f90007ba2122836c165e8b2b0d150137f5bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96c1d603c7de21f5be13698ea2adbfd943e6c65ef941d19add4452a3151e12e`

```dockerfile
```

-	Layers:
	-	`sha256:ecffdc790da72d467e322414d265ddaae4ab63b75f1443655bfbd21fd78503ca`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.6 MB (2587269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e2b54664e747ab93a07874a48860339e0050a99773717ba6093ca2b34b8eec`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

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

### `rethinkdb:2.4` - unknown; unknown

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

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:97d9fb8de872e30a1a9114c3b9491a4c665bf118f63bbe023a93ba1cd861f40e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d46194ae408e433a09b0ad64935707fd4d2f846a0f1fb39fed6a706a15a59ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898bb84fcf05326892fcfd6db7e48a19975d11ebecfb42ddb7443aff8b425965`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e11538b21c9e2d9ecc355c43addc9a13f176bd157d594cbb79fe48b9df7a7e`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 9.8 MB (9786535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65daa7e1b97965d06f434e1c660d22c523bdec7a69999626680057201cc5b2`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d93caa75dcc0a6337d79936b6408569234a5b28847836d4a5c2fe37e940c06`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 10.0 MB (9992815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ac91b69cbc57d5540e3004cc55a26baa1e99ce806c887a665dd57b7ac5237`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:02a0e1bcc1cfb40728d8cd87e3b7557b293373c6091cca4e3e55bd7fc8d97096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347f8992b84b8c37b4173caf3494ff6eb33e8a9558a16e9bfb0f2f0cf7e21956`

```dockerfile
```

-	Layers:
	-	`sha256:18ac5c2510de93dbb3e2ea858b022cac72864cc49ede34da12e05f3c1e28723b`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 2.6 MB (2586935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d43f7465724b4effcbc5e1c15c96bf19f19887f65709a8e740d6a3859ebee4d`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:7b56d11a281f1e837261d59a15f571be54e8a5aa4b0e875afaf06ef9f17c8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c088906bf631659e01c8743f3efc6ac3ed890eadd759f17557bea4defd57c79a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff3c58159d927eceb79f51c8b36d5a57c533f07869ccba15b528e638dcfc4c`  
		Last Modified: Tue, 02 Jul 2024 23:05:53 GMT  
		Size: 9.6 MB (9586083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aaa396b94a8c2a9ebf6805673d96eaeab110cf9f83ac46992e2834693f2b98`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddb798fede4afbff8c0e74d1d9b6147194e79ba58b0d5094a5cdabd2cad7a9`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 9.4 MB (9362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393536def3696bf836ed6d35f9d03bf67ad0f0d6767da953995bbcf580d3e19d`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b895f110e78c3960769123c3409f90007ba2122836c165e8b2b0d150137f5bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96c1d603c7de21f5be13698ea2adbfd943e6c65ef941d19add4452a3151e12e`

```dockerfile
```

-	Layers:
	-	`sha256:ecffdc790da72d467e322414d265ddaae4ab63b75f1443655bfbd21fd78503ca`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.6 MB (2587269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e2b54664e747ab93a07874a48860339e0050a99773717ba6093ca2b34b8eec`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

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

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

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

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:97d9fb8de872e30a1a9114c3b9491a4c665bf118f63bbe023a93ba1cd861f40e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.3` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d46194ae408e433a09b0ad64935707fd4d2f846a0f1fb39fed6a706a15a59ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898bb84fcf05326892fcfd6db7e48a19975d11ebecfb42ddb7443aff8b425965`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e11538b21c9e2d9ecc355c43addc9a13f176bd157d594cbb79fe48b9df7a7e`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 9.8 MB (9786535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65daa7e1b97965d06f434e1c660d22c523bdec7a69999626680057201cc5b2`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d93caa75dcc0a6337d79936b6408569234a5b28847836d4a5c2fe37e940c06`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 10.0 MB (9992815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ac91b69cbc57d5540e3004cc55a26baa1e99ce806c887a665dd57b7ac5237`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:02a0e1bcc1cfb40728d8cd87e3b7557b293373c6091cca4e3e55bd7fc8d97096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347f8992b84b8c37b4173caf3494ff6eb33e8a9558a16e9bfb0f2f0cf7e21956`

```dockerfile
```

-	Layers:
	-	`sha256:18ac5c2510de93dbb3e2ea858b022cac72864cc49ede34da12e05f3c1e28723b`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 2.6 MB (2586935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d43f7465724b4effcbc5e1c15c96bf19f19887f65709a8e740d6a3859ebee4d`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:7b56d11a281f1e837261d59a15f571be54e8a5aa4b0e875afaf06ef9f17c8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c088906bf631659e01c8743f3efc6ac3ed890eadd759f17557bea4defd57c79a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff3c58159d927eceb79f51c8b36d5a57c533f07869ccba15b528e638dcfc4c`  
		Last Modified: Tue, 02 Jul 2024 23:05:53 GMT  
		Size: 9.6 MB (9586083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aaa396b94a8c2a9ebf6805673d96eaeab110cf9f83ac46992e2834693f2b98`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddb798fede4afbff8c0e74d1d9b6147194e79ba58b0d5094a5cdabd2cad7a9`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 9.4 MB (9362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393536def3696bf836ed6d35f9d03bf67ad0f0d6767da953995bbcf580d3e19d`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b895f110e78c3960769123c3409f90007ba2122836c165e8b2b0d150137f5bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96c1d603c7de21f5be13698ea2adbfd943e6c65ef941d19add4452a3151e12e`

```dockerfile
```

-	Layers:
	-	`sha256:ecffdc790da72d467e322414d265ddaae4ab63b75f1443655bfbd21fd78503ca`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.6 MB (2587269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e2b54664e747ab93a07874a48860339e0050a99773717ba6093ca2b34b8eec`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

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

### `rethinkdb:2.4.3` - unknown; unknown

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

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:97d9fb8de872e30a1a9114c3b9491a4c665bf118f63bbe023a93ba1cd861f40e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d46194ae408e433a09b0ad64935707fd4d2f846a0f1fb39fed6a706a15a59ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898bb84fcf05326892fcfd6db7e48a19975d11ebecfb42ddb7443aff8b425965`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e11538b21c9e2d9ecc355c43addc9a13f176bd157d594cbb79fe48b9df7a7e`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 9.8 MB (9786535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65daa7e1b97965d06f434e1c660d22c523bdec7a69999626680057201cc5b2`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d93caa75dcc0a6337d79936b6408569234a5b28847836d4a5c2fe37e940c06`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 10.0 MB (9992815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ac91b69cbc57d5540e3004cc55a26baa1e99ce806c887a665dd57b7ac5237`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:02a0e1bcc1cfb40728d8cd87e3b7557b293373c6091cca4e3e55bd7fc8d97096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347f8992b84b8c37b4173caf3494ff6eb33e8a9558a16e9bfb0f2f0cf7e21956`

```dockerfile
```

-	Layers:
	-	`sha256:18ac5c2510de93dbb3e2ea858b022cac72864cc49ede34da12e05f3c1e28723b`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 2.6 MB (2586935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d43f7465724b4effcbc5e1c15c96bf19f19887f65709a8e740d6a3859ebee4d`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:7b56d11a281f1e837261d59a15f571be54e8a5aa4b0e875afaf06ef9f17c8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c088906bf631659e01c8743f3efc6ac3ed890eadd759f17557bea4defd57c79a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff3c58159d927eceb79f51c8b36d5a57c533f07869ccba15b528e638dcfc4c`  
		Last Modified: Tue, 02 Jul 2024 23:05:53 GMT  
		Size: 9.6 MB (9586083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aaa396b94a8c2a9ebf6805673d96eaeab110cf9f83ac46992e2834693f2b98`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddb798fede4afbff8c0e74d1d9b6147194e79ba58b0d5094a5cdabd2cad7a9`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 9.4 MB (9362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393536def3696bf836ed6d35f9d03bf67ad0f0d6767da953995bbcf580d3e19d`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b895f110e78c3960769123c3409f90007ba2122836c165e8b2b0d150137f5bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96c1d603c7de21f5be13698ea2adbfd943e6c65ef941d19add4452a3151e12e`

```dockerfile
```

-	Layers:
	-	`sha256:ecffdc790da72d467e322414d265ddaae4ab63b75f1443655bfbd21fd78503ca`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.6 MB (2587269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e2b54664e747ab93a07874a48860339e0050a99773717ba6093ca2b34b8eec`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

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

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

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

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:97d9fb8de872e30a1a9114c3b9491a4c665bf118f63bbe023a93ba1cd861f40e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:d46194ae408e433a09b0ad64935707fd4d2f846a0f1fb39fed6a706a15a59ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898bb84fcf05326892fcfd6db7e48a19975d11ebecfb42ddb7443aff8b425965`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e11538b21c9e2d9ecc355c43addc9a13f176bd157d594cbb79fe48b9df7a7e`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 9.8 MB (9786535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65daa7e1b97965d06f434e1c660d22c523bdec7a69999626680057201cc5b2`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d93caa75dcc0a6337d79936b6408569234a5b28847836d4a5c2fe37e940c06`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 10.0 MB (9992815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ac91b69cbc57d5540e3004cc55a26baa1e99ce806c887a665dd57b7ac5237`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:02a0e1bcc1cfb40728d8cd87e3b7557b293373c6091cca4e3e55bd7fc8d97096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347f8992b84b8c37b4173caf3494ff6eb33e8a9558a16e9bfb0f2f0cf7e21956`

```dockerfile
```

-	Layers:
	-	`sha256:18ac5c2510de93dbb3e2ea858b022cac72864cc49ede34da12e05f3c1e28723b`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 2.6 MB (2586935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d43f7465724b4effcbc5e1c15c96bf19f19887f65709a8e740d6a3859ebee4d`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:7b56d11a281f1e837261d59a15f571be54e8a5aa4b0e875afaf06ef9f17c8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c088906bf631659e01c8743f3efc6ac3ed890eadd759f17557bea4defd57c79a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff3c58159d927eceb79f51c8b36d5a57c533f07869ccba15b528e638dcfc4c`  
		Last Modified: Tue, 02 Jul 2024 23:05:53 GMT  
		Size: 9.6 MB (9586083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aaa396b94a8c2a9ebf6805673d96eaeab110cf9f83ac46992e2834693f2b98`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddb798fede4afbff8c0e74d1d9b6147194e79ba58b0d5094a5cdabd2cad7a9`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 9.4 MB (9362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393536def3696bf836ed6d35f9d03bf67ad0f0d6767da953995bbcf580d3e19d`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b895f110e78c3960769123c3409f90007ba2122836c165e8b2b0d150137f5bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96c1d603c7de21f5be13698ea2adbfd943e6c65ef941d19add4452a3151e12e`

```dockerfile
```

-	Layers:
	-	`sha256:ecffdc790da72d467e322414d265ddaae4ab63b75f1443655bfbd21fd78503ca`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.6 MB (2587269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e2b54664e747ab93a07874a48860339e0050a99773717ba6093ca2b34b8eec`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

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

### `rethinkdb:bookworm-slim` - unknown; unknown

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

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:97d9fb8de872e30a1a9114c3b9491a4c665bf118f63bbe023a93ba1cd861f40e
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
$ docker pull rethinkdb@sha256:d46194ae408e433a09b0ad64935707fd4d2f846a0f1fb39fed6a706a15a59ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48908392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898bb84fcf05326892fcfd6db7e48a19975d11ebecfb42ddb7443aff8b425965`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e11538b21c9e2d9ecc355c43addc9a13f176bd157d594cbb79fe48b9df7a7e`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 9.8 MB (9786535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb65daa7e1b97965d06f434e1c660d22c523bdec7a69999626680057201cc5b2`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 2.7 KB (2670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d93caa75dcc0a6337d79936b6408569234a5b28847836d4a5c2fe37e940c06`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 10.0 MB (9992815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ac91b69cbc57d5540e3004cc55a26baa1e99ce806c887a665dd57b7ac5237`  
		Last Modified: Tue, 02 Jul 2024 03:26:12 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:02a0e1bcc1cfb40728d8cd87e3b7557b293373c6091cca4e3e55bd7fc8d97096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347f8992b84b8c37b4173caf3494ff6eb33e8a9558a16e9bfb0f2f0cf7e21956`

```dockerfile
```

-	Layers:
	-	`sha256:18ac5c2510de93dbb3e2ea858b022cac72864cc49ede34da12e05f3c1e28723b`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 2.6 MB (2586935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d43f7465724b4effcbc5e1c15c96bf19f19887f65709a8e740d6a3859ebee4d`  
		Last Modified: Tue, 02 Jul 2024 03:26:13 GMT  
		Size: 13.2 KB (13247 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:7b56d11a281f1e837261d59a15f571be54e8a5aa4b0e875afaf06ef9f17c8f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48107894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c088906bf631659e01c8743f3efc6ac3ed890eadd759f17557bea4defd57c79a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff3c58159d927eceb79f51c8b36d5a57c533f07869ccba15b528e638dcfc4c`  
		Last Modified: Tue, 02 Jul 2024 23:05:53 GMT  
		Size: 9.6 MB (9586083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2aaa396b94a8c2a9ebf6805673d96eaeab110cf9f83ac46992e2834693f2b98`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddb798fede4afbff8c0e74d1d9b6147194e79ba58b0d5094a5cdabd2cad7a9`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 9.4 MB (9362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393536def3696bf836ed6d35f9d03bf67ad0f0d6767da953995bbcf580d3e19d`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:b895f110e78c3960769123c3409f90007ba2122836c165e8b2b0d150137f5bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96c1d603c7de21f5be13698ea2adbfd943e6c65ef941d19add4452a3151e12e`

```dockerfile
```

-	Layers:
	-	`sha256:ecffdc790da72d467e322414d265ddaae4ab63b75f1443655bfbd21fd78503ca`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
		Size: 2.6 MB (2587269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e2b54664e747ab93a07874a48860339e0050a99773717ba6093ca2b34b8eec`  
		Last Modified: Tue, 02 Jul 2024 23:05:52 GMT  
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
