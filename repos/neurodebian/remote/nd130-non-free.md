## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:b655705ebabaf2ce3541737bb5aa50a434bc498db4e71d21e78df6f65276dd87
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
$ docker pull neurodebian@sha256:2345e9d5aef9bbd8d5fce685c875b87cd8ed38310bdbf275f30cca1737fa3a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d597a16ff660ee441ebb22d3b5bb180c902805200ccf1292560255191a5119`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec6206d450964491a7487cc2c8b4f2d994ef88606a151b06667b29523f578c`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 10.3 MB (10292928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bce8330f04da576bc446171d4d85bc2cb33d4a1a8355f2dfcec201ce53475`  
		Last Modified: Tue, 07 Apr 2026 02:01:35 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529612aeb6812b0c6d4163ca3c7a25ff18656319204675ea597093c2b448ee39`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1c90309da3f2798b43a125418e184e41332d88d07ad27de08314749cbe727`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 90.4 KB (90395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1975e8b7aeb2feea22d9bdd8a88f171e1a11c1c03731143a067e89182c6f80a8`  
		Last Modified: Tue, 07 Apr 2026 02:01:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3499ca84d0540454357e462df180fc71f6ca058f826cc3918bf9199ac4065950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158f867a7849bd7d777618e51b2b411cdf63e44258290d824a82443276cfc38`

```dockerfile
```

-	Layers:
	-	`sha256:02878bf7b801891ae222e99167a7e34c7d90a16ee7df9d50dd57627bc41bfb1c`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93c033b100ba18fa1703dd7a625a3839348e09e6b845205fc3a60e57417137e`  
		Last Modified: Tue, 07 Apr 2026 02:01:35 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:93956c4f4fe270b0360744f841d3e50a69c757291c5adcac1b9cedcd068be733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b510a388077c96bf533603818bbadd3c4d8094ccc4fcfb0a3fbae74c2cdbff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d9f60605ecd6ecd594d2869043d5aa85a244922d2cb11c093c4c62ecbfacc6`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 10.1 MB (10077968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5997a6608cf7f8ac648a62e4bca2bd6165adbaaba00f4e78b3a2cb78035c4184`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d740ad08fd52abbff5ee50f1b915facffd710027e5ae2b07068b9852d643bed`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b8900b668d89259fed01570b11b7cddaad65b3a841629706a527867ad9b0ba`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 91.0 KB (91006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133814aac1502a11214ce7e4da9bbc7c2e1c97e1dc53b1e797ae8dfd4289a0f5`  
		Last Modified: Tue, 07 Apr 2026 02:04:34 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b3afb21138d7ee59554afb0bfedbded2fe517cb2f53227d81caf194f368d301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da62f7d9059d50ef8e12afa98aee31767e6e94fa186aadec735578f6aeb5237`

```dockerfile
```

-	Layers:
	-	`sha256:c342d94d37429180b3af40ac9f600ca6ee9bc518d5e59bf5d7e9f9ac9ae6d546`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2cdc4976db034f9e92a88cb5c57d816d6e961b1fad6db225bc78fd9df421eec`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 16.4 KB (16432 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:cb19cf363ab16c0a4358512bd0168fc0ac29b5a94a664aea4870cc8fb35413d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61380228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9fd486bd8c29504ac708615ad12390f9cf8e63beceab58a078f65b45ead967`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767b01bedb93f2d58ac04f7ac194ac8ba7658652b5f26954b88dcf1de2069b2`  
		Last Modified: Tue, 07 Apr 2026 01:48:34 GMT  
		Size: 10.5 MB (10467061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e9095ff2c86640af37247e8b0503adb4a924a7e77a231fc9a0d5dbe2f753bf`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f12721908b18e9c6e9b6ceae633014052eeaecf3932e098fd33b5c039692a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5012222bd8055762234bf5f4cc28f45026d2d60fa64a2da6df5ffe8d611ade`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 90.7 KB (90728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80e0fa139017e2ce92f74f9470029a9ab27762890d4cfc1136536f0ed6db017`  
		Last Modified: Tue, 07 Apr 2026 01:48:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:464b42572321f94f8cf7a4b02fe3edcaebc6f35fa1a1dda491e647463f400b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db9894f53becac279fcdee615966697296b694d316e46d18297f52df1c09a02`

```dockerfile
```

-	Layers:
	-	`sha256:e9071191f1c485726100f970d753707baf500eaea552b82c0c71459b3e35b801`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9c751f6adc1474b1cef7b2048a842ce49333f2e7257f14d2814990772b8ffe`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
