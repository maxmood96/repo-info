## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:f1f3f65be806cd2e5289859430967fb45d2c86b81d8f9e5647f088472979881a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a31f245a8e23ab333d0cb91a20812909e691960a320848d4ef26b352815a7a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64976262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f8d51d8fe2e0b29833a6930ee9ed8127229396c7bf674da0550ba14789465`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cb8ccddb7ae905a7c15a308bcc5010fd4a842839e6c4e55aea5037fc2c6f88`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 11.1 MB (11103489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73aec67b21a1a6c0b4dc177a5965f48251ca61285c2843d50601d15bff859db`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f906aead18b295a02b3010f8b914a9b91159b0bda97419216db9f38e2ad3d90b`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60969937977bcc4c5b60c1148c0bc24e73935eb4543bc321604bd0cb403bd1a`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 101.4 KB (101372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dbca80d9daeba4dc863e30e3d1b11e83b590a71f2404c0f81f620de94f8861`  
		Last Modified: Tue, 19 May 2026 23:26:45 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4c7c72ba8aa60242c01595e6c329c6841fdb75347d3a378338e8f79168111c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b351f919e5d6f50af1abf13db25055742b5206b749deb69a8512c9483a9321`

```dockerfile
```

-	Layers:
	-	`sha256:2f85224be519cfcaeecbec362461b06c554dec6c914ac74dc25ea1b39c2399b1`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0003492d33be36dc5b18d246a9b0ceecfcdc28900cc4527fde33b969d8b65b6`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:44ae51ff793f39946038ce5d95af869b3b70558a685f74437925423722dfc75a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63470348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818e4b617c895bb6f2e851ddf2b7aa3e84a209b97a6f73727ac44d87e804840`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:30:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ec49c2c0e7ae149d1217b1064a04894098733733e47129d491b619501080bc`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 11.1 MB (11109941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221195c4a3803c742597ae3c20c7938603d4225ba8bc12e2a132e14ec3c1534`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3976723b40480b65484fdac4ff3b9cb3f2c4adfaad97bd5fcc0ce764f71730d`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30ea5cadfabf914d41176cf9b67c2e8c84268162895103d5f5a190a1c91f259`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 101.3 KB (101283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f656a055002be466165c33f521121cc4442274cdf721654db837483142b402e`  
		Last Modified: Tue, 19 May 2026 23:30:31 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a1a1bb1d584fd6181b16c73cdf9c96191c3e2364aa67a79031ed79b692977be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e012ba92c198995a31023ae78735740956364723a16b42738cf90b5bf0d33866`

```dockerfile
```

-	Layers:
	-	`sha256:14bbb92d22c5cfb94345cfb92bdf1472efdbc687a191ad6da80b3deb70706234`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372972fb25a4fc5ab5ca9c1eb667e639300981bf1c0f0ebfe6758a13599a0111`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:dce71c3d3978a2a855abcf1bc5a83a54b0f1eb84afe9c708d37b9945612e3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66315350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0801860e74bdd4e1248165adcc97832ff1397a208cb4e9e22f057ff56cc487c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:25:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:25:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:25:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:25:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e09eb609a6245c10b9cb43e597a7ec3d9e4224f925e717a38f2fb36787a4e7c0`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 54.7 MB (54709050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95b0b4b40e146641da97fbb635272948b4c269cec26aa79cbfb54c37dbe1649`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 11.5 MB (11502477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45354a9aa4ef78b02696ceb5c8a0ef10d0988ccf5c880ada568b69ece7d4c16`  
		Last Modified: Tue, 19 May 2026 23:26:04 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987dc208402f1ea8675711285765d6168b97248acb8af9055c80f2d60ce40408`  
		Last Modified: Tue, 19 May 2026 23:26:04 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6f4d36ca15503abe1f07e2b4c2b1de0779f2c0637b548f8b311632e249513c`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 101.3 KB (101276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb5a5de4f9760cf73bff4a94a316eb883b68e28b6e15d06881dcef89e8ea279`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c9a4a7d9ac0a43c6ef88e5f3f498ce786c0ecaea09f7225e425e6ffb3efe7e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b511300d3fa88ec3da28b7d91942be85641b4ee4e5e05658b51c195e548a2da2`

```dockerfile
```

-	Layers:
	-	`sha256:d1b2779cbb92980bf8bab7aece37d6ba04e04f00759c3ad6b8a4de4bec717427`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715cda405a610752bcc00c2ba1c11215cf139bdc737d545c950bef4d1c5f0117`  
		Last Modified: Tue, 19 May 2026 23:26:04 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
