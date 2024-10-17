## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:15e97f090ba1169a68968f910a456d648443b1059e938a5bc247354280ee4f41
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
$ docker pull neurodebian@sha256:8405eb81d4fb50f2e0ca8052e64751a2166bc5f44bd91dfd5f8364928076fca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59959165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b6fc36a6afd9830924df899db96464eff91a08d2fd009cb9b3d1088a5325f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
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
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1707618fa9372fa7563234001ca06291da815e7c963e11719d290dcc36218024`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 6.3 MB (6270740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f92dac85afbe3987da72fdcff7499ef9a4bef39d0ea83f70ad579e421b2b1`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560ef25c1ef36b5b05dc1fd297de1698589349e5c080811754da6ab61635771b`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c67a14658f20791e7bebae65768af2451f13d17e95b1fa2ffbcd886802abb3b`  
		Last Modified: Fri, 27 Sep 2024 15:30:29 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed1a0ff889a3d19ad950be2e4cb5a585ad9f69009887c6d58da8a5f7bfb5ed`  
		Last Modified: Fri, 27 Sep 2024 15:30:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a0fb2b4c94881a145a88d8cc5d383cc5abffb8759ae1bbce2a56aa27dcc36e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fea4b5d7ea7ed8b0f6ce474f3f3263dd4b2b04738558dccdd3a704db4e1b350`

```dockerfile
```

-	Layers:
	-	`sha256:0b580fb68668f72246a5b77f9ceab789100d2ab9171a59039e674ffc2dafe1b0`  
		Last Modified: Fri, 27 Sep 2024 15:30:51 GMT  
		Size: 3.5 MB (3543111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ccb2a5d05b136f255c231e5f7370718d916c8cee58b2a409d354d4a1fc598a`  
		Last Modified: Fri, 27 Sep 2024 15:30:50 GMT  
		Size: 15.7 KB (15703 bytes)  
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
