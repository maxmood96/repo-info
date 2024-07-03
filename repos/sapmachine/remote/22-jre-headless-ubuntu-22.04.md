## `sapmachine:22-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:868b4363f0e733a083a5b7a9f62dc44a0a10965ffd951809ae5272ed46126c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:51a5f21ec0cc46a8c0b92cb91abb4d0183908c0fd2e57cbd468e8446d3b1e64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87641852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3e8c51ef878935b0ccde21e4bce87c7664c48e5429923108ceb4e58f51d81f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f473a9179361515856cfed346b9d843ee54067f398df129408de9dcbd53ae0`  
		Last Modified: Tue, 02 Jul 2024 03:31:29 GMT  
		Size: 58.1 MB (58107797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aa3d3fc7e8ebdf1ee7becf60917f59ba4e2feaff87b3f8ae22fc63b9d72b8ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff6a2ce5a038351882985e341feae2d181d6fe159a24cf287c06ea802533423`

```dockerfile
```

-	Layers:
	-	`sha256:8e85235411360df8568f6aa994c4c8e790699e20193e8b95d52d118f020efdcf`  
		Last Modified: Tue, 02 Jul 2024 03:31:29 GMT  
		Size: 2.1 MB (2121971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2aa913e7350c1ba542f695dcb42f86eb592696d6dcd9f30a218a3425714a144`  
		Last Modified: Tue, 02 Jul 2024 03:31:29 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:bccb240168f7c89da447c300f33771fabe03ab0768246a8d21dcdf05e3702f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84465623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1291e09b2d34080640eb0d8e4b47e3589fda14a75680083cfeea15f72cb84fa`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7d2bba0a01c510877f456fe68b1e765b80510cca8a5d69fd1d19e860cf1499`  
		Last Modified: Tue, 02 Jul 2024 23:57:38 GMT  
		Size: 57.1 MB (57105598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:046586d2c76a53b8b83d38980ff841ac619795123dad3ce39760a8010f3b7744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3d995c63eadd98a2d08446e40acbd433521906033f15342ed9052be597d5ac`

```dockerfile
```

-	Layers:
	-	`sha256:779c551fec6f6f22cda8393920cb251e185784a02803f33308c44b57dba869d6`  
		Last Modified: Tue, 02 Jul 2024 23:57:36 GMT  
		Size: 2.1 MB (2121034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:483abae09207329cf458fe82047d4949fd47b03e6f125442b32ba080e564af4a`  
		Last Modified: Tue, 02 Jul 2024 23:57:36 GMT  
		Size: 9.7 KB (9700 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5ebc3cc81c19f43f5a88670b7b1c63f99ba55a979fa275fc307b87af59fa4182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93829772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca37c8a29b4e39f63c4436cfa57524499f085c88a9a40b88b3cdcb178647b3b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51259b9fed21f163a9934ddfa10eaca7a5f415dcc0e30ad8db3822f46c764d3a`  
		Last Modified: Tue, 02 Jul 2024 21:23:44 GMT  
		Size: 59.4 MB (59368691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:776040d14e0590d5a40973b957731cdd03ecca1e4929eddfff8d70ed0a816718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4098a8b691918ee7c64a7ebf7c6e3a6a9cd5ae5773f3640dcf87abb7684e7c4c`

```dockerfile
```

-	Layers:
	-	`sha256:be199e5fc50879d62432dbfadf0c162cee48a6f683a9f3072bb584848c8429ff`  
		Last Modified: Tue, 02 Jul 2024 21:23:43 GMT  
		Size: 2.1 MB (2125261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aa9cb4e157bb090e95ecf8df9d1ae1347c1d63e7b2bbca56ad67ff8b3d2a20d`  
		Last Modified: Tue, 02 Jul 2024 21:23:42 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.in-toto+json
