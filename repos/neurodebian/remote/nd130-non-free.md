## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:b30144b25b4f9eda8cff7e3527ac291ee12ef4085cc006a28765cb84aa420700
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
$ docker pull neurodebian@sha256:a1f3d681375ae9877cb174d624d1c5cbd04a741b1cada66a9dbce8265700d3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59671672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ee6736859c305f7a5a63b3b9e54bdb047bf11407b4ec44ead45a2ee482f2e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:33:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:33:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0719b276ab21986970910cd53aa98e1720cae839dc3245e4539f6466de5586`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 10.3 MB (10292332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4019c5b48e86642c8626c9b3af0135436b974b87db9eb8192ded3d7ef13afe`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc68ef74c45ffbb305959abee61f51b007da4b83b356f90740ea0a7a315015`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f5af02919eace9dd5db853e2f41d073cd35d27d1c0e8b76f95ff2f940f3dd0`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 90.4 KB (90370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307a513dcbfdcdcca80b9eceb62b78bd4af37a8672d7420381d085405a3dab7a`  
		Last Modified: Tue, 13 Jan 2026 02:33:29 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9817b4cc23261bdf6af3b2b878eac1bec5c62dd85db0d7bd7df14a6039a2817e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0565ca92f711426185538e4fc88ae99140917adec4068a1fd1343dcf23797c4a`

```dockerfile
```

-	Layers:
	-	`sha256:3fdaa0bbf6cb71883d44164a4f5068383c9f11b3230e9905be8b678a54d1ff65`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 3.6 MB (3614108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc16a4a69d2920022ac713a906e760a6cf6c371075d6ad1f69e3a8198569a3cb`  
		Last Modified: Tue, 13 Jan 2026 02:33:28 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

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

### `neurodebian:nd130-non-free` - unknown; unknown

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

### `neurodebian:nd130-non-free` - linux; 386

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

### `neurodebian:nd130-non-free` - unknown; unknown

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
