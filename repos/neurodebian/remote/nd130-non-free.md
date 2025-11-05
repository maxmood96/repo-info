## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:054cb83bc13a514b14b0d6d2127811bf8c518e556fd6edf1c54b48aefeaff471
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a84e7c70d72128f0303fdb503e24ecd7c72e91d03ce7d2d107f71fd126955cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59669100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ae6b2236202b62a987ca7ce3e3a621ebf3b0ea0f954e6b7b038687bb9f71ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:17:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 04:17:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 04:17:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23386e12d6e309376ac1a14efa640269690dc204b17984b14064c2fd2f49098d`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 10.3 MB (10289939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4a65b6a6351a097123b770a2e0e8e7d5c03b57aa5a1dad26e1c2eadaadfd28`  
		Last Modified: Tue, 04 Nov 2025 04:17:39 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52742b84510725699f7a178b63e604e0d0891893d1f2eb344188531d8636f0e1`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aee8c1d05553c1777be79055a18fea90ee2b8ea9411f6c738c5c18eba8d1c6`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 90.2 KB (90186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2b299738c4e4019fbb06b267440b617ca810b6d56b21bc0afdd3695d852ada`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0089444d554e5cae9f22a559edef3bfd16e1bd0b68860b6c214e2428014781d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba98d48bfb433fb8f9a10e0d06f0d683a5c4944286fdaf551bce2c5892d7022`

```dockerfile
```

-	Layers:
	-	`sha256:3c66055059d16bf03b067f48cf3c4b38abaf5be7f3bd7af8dfaf7d94c8708e01`  
		Last Modified: Tue, 04 Nov 2025 11:09:30 GMT  
		Size: 3.6 MB (3613075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64a75afe777c95a9303af2be30b3244166f9507b5d307bc436cd2c311c33b53`  
		Last Modified: Tue, 04 Nov 2025 11:09:31 GMT  
		Size: 16.3 KB (16280 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1529a63d3b1fd5b20e69752735685aed7551980815e4f5ba9dfeb57bf08a98dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59818048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede29356c99f4ad500f6f92d01d99c80598e7a0ab06e0cba76bb427bec98bcdd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172872c0ee5e3387027dd024c77e0a566ab9e979918d5d1ae3a862912f9819cb`  
		Last Modified: Tue, 04 Nov 2025 01:32:37 GMT  
		Size: 10.1 MB (10073407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd94c5bde5357bba8d2d736f7e486405a517a770df0fbf2434fff09e3cdfd82`  
		Last Modified: Tue, 04 Nov 2025 01:32:36 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3686e47e17b33cbec471ea4f8d20ee610283524c8e381b60bbe0bca643d3cb`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0201931aec9ab3ac74ff7c1fcb5bbda1b95323d45a16ba0594b8586855f134`  
		Last Modified: Tue, 04 Nov 2025 01:32:36 GMT  
		Size: 90.9 KB (90860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda921f974a2bbf05547e240c45b797d09307a80d64747669b300890b4877699`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:171c082cd86f6d465311384dc89b6f8caef5ba756bac4b22acc5740480c28923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bca970acfe0d4594fdb6fa5375fc79bd72f1c0309d3fcd6644884295e7a995`

```dockerfile
```

-	Layers:
	-	`sha256:e6a4a640a7d1de22f588ad1235c812b9907faedeac55c9b05d4fc71a53fe4317`  
		Last Modified: Tue, 04 Nov 2025 11:09:53 GMT  
		Size: 3.6 MB (3614602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11690b726c377ad7c6177f469ec7805bdb379cb0e37fd6d69b8c57d618893f46`  
		Last Modified: Tue, 04 Nov 2025 11:09:53 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5771d15f06fa62ffa39ee92437de3260e58824c9c3aca71b930f2340dd55319c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61357929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae41e42556a48153e417d850113110e79e617019f105a3699f765baf91edbacc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:38:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c3eaf959f47b3c81adaab22c02b91552da31d1998da6c88911ad6288b7a9fb`  
		Last Modified: Tue, 04 Nov 2025 01:38:50 GMT  
		Size: 10.5 MB (10462757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e9ef740b4bb48f2974e682a417cb34fceb185aca217d1c2c7f6227a748dd40`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242bf4e4c9cf11d3df4c63f4db58331b50dfdde7542f70fffe6271a6cef67b5c`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7804e0ac9d5bfb67777d18126743dfa3501a6cab30e2779e9c1e882d3931d3b`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 90.6 KB (90584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f31b454367cf57f9fdcbbcbabe35b3a537175a9cbf95e0455aa5c68268299`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fadfe623ab9931f7482ec50383c61bca36e19d1881f7b599d5a47feb0ee6dd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e8ea8d062af83ff955f51cd8b7f77e408cb8628ee432dade259fd59a85c1b7`

```dockerfile
```

-	Layers:
	-	`sha256:088a395d40071397cf8e0032ab14cbcabec0416a8a0a34130b1268e1fe736e89`  
		Last Modified: Tue, 04 Nov 2025 22:51:34 GMT  
		Size: 3.6 MB (3611024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc01ac211e92ee4d0d4707e08a6fb4c64315bf3561a027a8594a15e46d12b72`  
		Last Modified: Tue, 04 Nov 2025 22:51:35 GMT  
		Size: 16.2 KB (16246 bytes)  
		MIME: application/vnd.in-toto+json
