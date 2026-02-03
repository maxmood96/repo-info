## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:4bf6259209bc214c61d034c1dc11a5f99f24c56694fc40cebf1fa4e991e82640
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bfe6f18aa6a74c90c1bef54a8ecbfd1554d462da56f4431077902cee7e35743f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59679073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734174826d480fd0ca4221a27524fe98e871a54a19c068307ec6b8d151189d5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:49:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f763d27f0cca3eca63d032df25da1781edc10ad21bb6ec6472a87765b5d494`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 10.3 MB (10292413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2193d3bb29390a43b5fe3cf6ef36f5d049269591f33a3f65f1c3ebf33ea628`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f82edf0cab6319880f6003cb047a9679b2b534d136feeba495550f279df6cb9`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae03b3a868a98138feda4a04a1f015e865a3599f8231275cde4e2d3ab18157`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 90.4 KB (90354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f2df40ce739fcaf54c09cdf8f844f97b7b89ddd3a009cf66056798e7a816d`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fbf95673c18f9bfa0a30481eb45b538fec3995c608702a1c1d90e08da42446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9f83b2f6643450c6e9f512971c820c8345c704dcd2e8cc7a8756a02e736f86`

```dockerfile
```

-	Layers:
	-	`sha256:6c76910ec532300ba0ac33261e0fa300df86a2a7236c44063bcf717e3999b372`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48dd7f90c47288d683499a84f5abe7001a411496c218e1bd8e77b25b0888176`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3e8b1aee676dde93acde9fac58fa3ab60f76be22359149b15a158f66571828b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59816200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e16820c26affbce98ddae6fa99af774b35f36fa48f83f0175f7cc280513d9df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:36:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:36:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:36:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:36:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ed602a8d82e45752b42458f6c6cf735a34652ba4dde594e695631d834d59b`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 10.1 MB (10073712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8fc00822d28ca96ab3b0a281c9f30f594ddc2a1097c1d118b5a8d327ade838`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8209c0e736639a6f4be8dbb64c8eebcf8f0660d2bfc6801b3c25864d8deee2`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850c1d0537909467bd63adc7a9f8b6c380009301140d89edfcf9e56b6a682db`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 91.1 KB (91057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f820caede12aa6a0a73d704ba9b536c2a46a1c60230cf73b319c81ab1626f30`  
		Last Modified: Tue, 13 Jan 2026 02:36:36 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9e27486911deee56ba88782a368ea64fb2d4cfebf43f5046a845fd248bd042d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ee1f59febf6225a8b47ae664b8af048babe29a052e8afed5aacf201038bfa7`

```dockerfile
```

-	Layers:
	-	`sha256:f6eed23b2bfe38aa7cbef27424d9b0bedeef111763c3f9036af89d8ad36602c2`  
		Last Modified: Tue, 13 Jan 2026 02:36:35 GMT  
		Size: 3.6 MB (3615635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df7281df837c359d65967773d79bc4901995aad5084db01a47562adb7c7d61c`  
		Last Modified: Tue, 13 Jan 2026 02:36:36 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:0e960ee0faa42f6bdd57961fff7557121bcaf8613b82e9b199d40d7a0261d96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61359689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571fe39bf716fc3e4014c560ab9d7be66fbb4dc330c7f227e15b9de763fbdf3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:12:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:12:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:12:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6161421471c9fb8d6e355616caf09b7087ac27ca53984bcd4134a0b0d7e111`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 10.5 MB (10466725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ebcc0e9e4361a538531fdba9070f9175a771b5bb299631b4e6ba78b8981ae3`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895adfd9029fe52f402919d58a03065389e5be8bff8acbf6465d5a18b525fef2`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7e6cefa33611a70c52fbfc73b63e42b2cdfc1fba6226f458dc3f5c739c142`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 90.7 KB (90740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3130aa08749bed8751f83a3a79d2ab7115ab45e908a1b0fffbdd9f80014cee1`  
		Last Modified: Tue, 13 Jan 2026 02:12:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e78e25dbca6377a9c55bca652f94e0e9be3780e215df940fb294f1d5d86968c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f5b3a6f545f0eba153876fc40fb4cce27fea22fc5fc61617969ef489152f6c`

```dockerfile
```

-	Layers:
	-	`sha256:847768114c721eaa57ed7d191df816ead0fde24426576323ca0caead4f71653a`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 3.6 MB (3612056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34278bc983bca66a2b8695d2725d6c0031354a486b9d39d322df70ee7d8ffc6`  
		Last Modified: Tue, 13 Jan 2026 02:12:26 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
