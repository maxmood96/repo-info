## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:bad71016f3e866855f3587fd24d490993b1a5f42559f3bbde1a824dea9246217
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2539128c80ecff27373893ee6f6df4c9a96506a504497cc3af31b05824272ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59679883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8d6ed4cfff9d1bf0d86cd7b60e22e65822f17972de2e91d5b473700aa15a77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:38 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d617f6a0a797854793d7e06246eaa1cc7a274b169099110596824813b24681`  
		Last Modified: Tue, 24 Feb 2026 19:26:45 GMT  
		Size: 10.3 MB (10293009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca86d8f4f35d66f7fb3dcb37a48634fa7de00cf79c56e801bdbc831883fe6389`  
		Last Modified: Tue, 24 Feb 2026 19:26:45 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0920acfe6dec5c0fa87633d7a2af1c8c9c43438d5bd243693756e37e463893e`  
		Last Modified: Tue, 24 Feb 2026 19:26:45 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909574c28df99449fba2623bc286e18e5e1472a8e0854ddaccd89f278bdd1577`  
		Last Modified: Tue, 24 Feb 2026 19:26:45 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7946a66ab124857ea36bdeaf15b5e92e15f2de95f1872c018095dbe2d4aba59`  
		Last Modified: Tue, 24 Feb 2026 19:26:46 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60f5465ec880ac8d520e20328a83c908de5c76f559d5ac306ba37aadc65ac642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54be4a5a1d81f7a94e7bb7e20c43f504abe01f552665a9a8c8b659cc0e55ed85`

```dockerfile
```

-	Layers:
	-	`sha256:faf5b1420a2e955c51824eb5cd04b3555983f1a1d32bad23b9a17cb23d227199`  
		Last Modified: Tue, 24 Feb 2026 19:26:45 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62f54a05c83bb7808e87eb9163ca563b16cd840bf7b4c2155540639af682850`  
		Last Modified: Tue, 24 Feb 2026 19:26:45 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:93f33e1d7dfcd48bcc1d944033444c0ed9a402076a77e8c0cabd146e476bfce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59824568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cc0cb9e70eecae92fd2fc17d7a789498b2479548ab9ddcf5521fed048fce2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:31:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:31:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf453ede294d186feaf250d77aabeaf726b6ced2aa9fbe2e5fdac4b1f84d42`  
		Last Modified: Tue, 24 Feb 2026 19:31:34 GMT  
		Size: 10.1 MB (10078025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30928927902d268262b08b5efcefb89e4c3617d22efa9b8ac761a0d7525d83cf`  
		Last Modified: Tue, 24 Feb 2026 19:31:33 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdb6065b1e1b80bb627ffc5c6033fafd6a5baf3deec6b393c5d48d77921d00`  
		Last Modified: Tue, 24 Feb 2026 19:31:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3839dacda2bc4228e929598d67b59e6dad35621e63c6783dece92c970e1e0b2`  
		Last Modified: Tue, 24 Feb 2026 19:31:33 GMT  
		Size: 91.0 KB (91025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d87241c55aefaf19d6269309249912e2bab24b779a5be0815dac4f0283d9529`  
		Last Modified: Tue, 24 Feb 2026 19:31:34 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e0c8c4f10584252d31f5b613bc3ee86962348ca54889a113adc79a72bfab1069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d36ef81373135b2e2653e741648f35618d865ba28ce784aa4c3409ae76e982`

```dockerfile
```

-	Layers:
	-	`sha256:5b50468d0bffcd89908ee2d3aa312549982d4b15e5f818fbd908135c28658df5`  
		Last Modified: Tue, 24 Feb 2026 19:31:34 GMT  
		Size: 3.6 MB (3615635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41031d043f8fe98d5a06eead883ae528ccf91e1f9c8ae5b81811ad5f1eeac98`  
		Last Modified: Tue, 24 Feb 2026 19:31:33 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:04a49447612026f03a4c076179e385694cf9b6cf75fb593ae68cceacf03c1f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61366502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a18ccd24ed577b412b5b227a5f2a3f96245f21eb84192da078d4db3b767ce44`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3269cc74f254412d24727310304f0bcef754b3e224a553bd10922741717c244`  
		Last Modified: Tue, 24 Feb 2026 19:26:17 GMT  
		Size: 10.5 MB (10467138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacc8284e1e89c9bc0d207e83f592955848563eaf07a9cac5f13869430ded04d`  
		Last Modified: Tue, 24 Feb 2026 19:26:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c25dbd7b30575c565c00bdccd329d4e24d0ba2e85e13de3a7324fd3eb2398c`  
		Last Modified: Tue, 24 Feb 2026 19:26:16 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08104f2275be56a77b403637ce7b88c967c7f5c37a0a62b2a09ec6f0a8d28fbf`  
		Last Modified: Tue, 24 Feb 2026 19:26:16 GMT  
		Size: 90.7 KB (90740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32d926f891ea459ffb58cff05f6fdd6f456c187ee6ded7a8a81efd2d36411e`  
		Last Modified: Tue, 24 Feb 2026 19:26:29 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cdd804b111f93d75b80d61a97d828487b427ab918c2aea4e39421a102f170f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848d2ece437b20d4bc05d6004ebd3a3ce647a949cbd03d9a4509f79e89419d42`

```dockerfile
```

-	Layers:
	-	`sha256:72a8e3cbdb726bb0f3f0769014289ce2d43484ea184b4ea982c38ccbcf15c071`  
		Last Modified: Tue, 24 Feb 2026 19:26:29 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd16cf9c7fd6b34fdba3dc1b6fc038963c8a8a4637402cf2e522124657560d7f`  
		Last Modified: Tue, 24 Feb 2026 19:26:29 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
