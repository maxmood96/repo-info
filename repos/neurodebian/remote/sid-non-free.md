## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:f23847bbf2fb1f2064a746206684077fb8f9eeafc6b6e739bcbe6b759c9554a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b2551aed7873b42c6948e4b859e19766d92fdfa9124e197eb17d7e01396a956f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59654703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdde34f32b6bf6419324db05b4b8b5fb9b6351610e3fb059cee7f5bd4e5195f4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc7e4c0fdb6fdb4dbba108ecd5d312d29ef194ff9fcbe5d6b45de7caada7a15`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 6.3 MB (6289352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93a3157ecf2b3e90f14bb799e97539e5da9b8e54c2fa24fb906ee69c4f58f3b`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7faf9478aaf287f3c93ce350f01a65b610825764a68728311533510f3bc121c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dad48c7fe85a9fcbbcfc1c1083d15785484d25efd58f98a59df48aecc124e08`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 91.1 KB (91103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb07a3a2622e66aa964a597aa305a0c72a9f55414a983c902e52931a87bb172`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f0dc4fccbda04d9082a17dfdcf47af681064b79911dd81b78c74058479c14f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abd151be0aa00d64da82c73b693e2c7729a6a8a65244bf3815c4aa2a56aade9`

```dockerfile
```

-	Layers:
	-	`sha256:646ad1bddf77b612de799f8d4f963ed5e11b83eafd6cf611481dbda0d44dfe7a`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 3.5 MB (3529880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92efed635b4a0876acf283e7170082bb89d0f2d6f397ab3e4a8cf9fe8faa62bf`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 15.5 KB (15467 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e9b1dc92def9b23d4147b701479a4c0cb4287a99fded2945d0f6141c918d1718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59997190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e1d085caeb9723f2e7d1685e044ddfd1251b756793da9068dc8ef89912c923`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c4d641255ff6bd7b8ce630c8cf947966d1ff05bdf86f951c687f989e2f5e9`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 6.3 MB (6273546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c25f32db1b1126487143c75b9ce0d496e410c5bae14e76068c7767c3979041`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1aa1fca4ed404a2dafbd083628f990869ee0dd7b253df1199afbf67da6e338`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4cc25b7109f5af55ff37456e9f7fe94f979dff175b36667bc066bff22439`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 91.8 KB (91781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376ca4ce57be9758785676dd94566197e97b56e273d0d68b507106d5fb088f89`  
		Last Modified: Thu, 17 Oct 2024 13:32:59 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbb9f5c6a73482e60b6f663408c48da9384405cc218fc0247429a4db9e0a0c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f10c7d37e9b03e2031feb3ef71d8d1bf5349441266305f933b01c78e258c35c`

```dockerfile
```

-	Layers:
	-	`sha256:ae362c8599903d2c6f23db6caf041eec1d93bdbc004c5115130317bed59a413e`  
		Last Modified: Thu, 17 Oct 2024 13:33:00 GMT  
		Size: 3.5 MB (3530921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857190c4726e7bbad6a89b69d081e58436891e0510c537d4d585edd56bfece2d`  
		Last Modified: Thu, 17 Oct 2024 13:32:59 GMT  
		Size: 15.6 KB (15601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1a746becea805a95a3b1d8e2136c588c82f6640fabbf5b5d22b913ad88128d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60829482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fbed28d59a1fde84fdbeb100a9ebdf604b856235061876e877aad0b4be73e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035359a3193290ee93a025ca5d676f11bf3efa25b6fddf81d67bf8d3589b5028`  
		Last Modified: Thu, 17 Oct 2024 01:14:38 GMT  
		Size: 6.6 MB (6617986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952f46bac813925be650db4453b8ca209127d3493fe97170e8fdd998bebdc5a`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f6a0313c5de2ce998d42e460162c0b4dbe7db82dd1a2ade4329507eaa884aa`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627145859a1fd6976564bc212d417d5a9a021b48d6c5cd0a9c27f2f0c0be85c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 91.1 KB (91141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd40c06f31194f8a4e83082b6d1fcb10e09061c6020cf18bf235dbf216f4e048`  
		Last Modified: Thu, 17 Oct 2024 01:14:38 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5c4d6d229eff64c513e035a637fdf70b11dbed69d4744893382bb2d655526e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8763464ded6610a3ee8e5d2b2c86e7b273c0e22ea00d4f5dd76840ba5564328`

```dockerfile
```

-	Layers:
	-	`sha256:75b677fef86179ceeb75d8f6689cc441eac33fd1413684cda9bbe9c0e9a32c81`  
		Last Modified: Thu, 17 Oct 2024 01:14:38 GMT  
		Size: 3.5 MB (3526979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8a9cdb86f97778094b27f0215ad427744de8426832800947d789f3e3cb0c8d`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json
