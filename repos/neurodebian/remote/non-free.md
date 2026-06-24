## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:5ab9abbc868b8c967ee9bdba32fed05ee5826365efec8542ac60f267f7fc4cd3
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
$ docker pull neurodebian@sha256:c16033d5894ff8fc4b55745d1895b3dfe7ae0e2d0bb896febbce4ad633eb725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59705114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7b6176cfa134829e36159b2077538cb40925f1e2c7ea20241bb935623f5922`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:44:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:44:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa87f9784bfdfa222f8a2f0de0a5007a594a7d6da7e800bded0a1ee858d7cfc`  
		Last Modified: Wed, 24 Jun 2026 01:45:07 GMT  
		Size: 10.3 MB (10294106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d370942ff479deab55afbc3dc15231e370fb5406c72bc0107ac84bd58e67fd`  
		Last Modified: Wed, 24 Jun 2026 01:45:07 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee8a334b1beaa6c6661b604e9faaed8affacfb1b41700db99136853e315849`  
		Last Modified: Wed, 24 Jun 2026 01:45:07 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506dc927f1decf019551f5c85f4b61a2afe8894f8cd0b0c0259e1eeee120370f`  
		Last Modified: Wed, 24 Jun 2026 01:45:07 GMT  
		Size: 90.4 KB (90406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ed73052b2fb347d9f6adc312aed3af88a1ba9fc34b9d5fc3ab530517fb0f53`  
		Last Modified: Wed, 24 Jun 2026 01:45:08 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a8d76f49180c80298dc39b062100b0312d74cabcfca851092ca95912d96c1a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c774d2540d0ae9707b82b71e4b6f91c4f9be35ca9b2d8d20a0c6b7a935b90d`

```dockerfile
```

-	Layers:
	-	`sha256:e07ca4a41f3bf9c6697b4b52b56e6eca2e69a7fe408e1d2e81af5fa4ba3a6384`  
		Last Modified: Wed, 24 Jun 2026 01:45:07 GMT  
		Size: 3.6 MB (3614204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67bf15604d906bca091c812b373e0ff912c524289873d10d6b835f82b3b6dee6`  
		Last Modified: Wed, 24 Jun 2026 01:45:07 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e1b7336d1152f988b148e32442e5aff966ea043393c6db69f3416df34abc2f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59852003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376fa39221b6b10d31402e4775bafb210811b7e3e5bd65c3a78d6fe4f6213cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:48:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:48:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:48:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d30b3b982a47f971a69869bed1ee1ff394e43b96b7d6d1e59006710075c6c3`  
		Last Modified: Wed, 24 Jun 2026 01:48:59 GMT  
		Size: 10.1 MB (10079195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990ebb8b34a3dbad6ebc63594e951b0665a35217e358d4a2d872c79dbf7832f6`  
		Last Modified: Wed, 24 Jun 2026 01:48:59 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d412c65895e9719eb9ec70dbbfe3e27dbb14706b4f1b2a84d3a934c5ea89152f`  
		Last Modified: Wed, 24 Jun 2026 01:48:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d4618a8413cad3a44195b11e837a0c74d8b9a67c3cff4167c719f10b0fe5e9`  
		Last Modified: Wed, 24 Jun 2026 01:48:59 GMT  
		Size: 91.1 KB (91061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae49fdab44c557279e2faf224a1aaf256936ce951da15d75af7c8dab1dfc461`  
		Last Modified: Wed, 24 Jun 2026 01:49:00 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b6681c763ad36d4bc7d42e370706a23dcd1b763aef4daa69448a2145fddc96b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1c082653c6fa1791d575e1a7c572a7315769ec2ef4f872160a7dcbafd7475d`

```dockerfile
```

-	Layers:
	-	`sha256:1d5e593608435b092b2f5516efa4396f4fa3e2b72caed49be4fc22fb0876011b`  
		Last Modified: Wed, 24 Jun 2026 01:48:59 GMT  
		Size: 3.6 MB (3615094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e7c12c578700b059dd7ca7ee39e2f9f5494fa0da32eaa6da853f4006c3a81a`  
		Last Modified: Wed, 24 Jun 2026 01:48:59 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4ed0112526c9e2deceb040e27a68d4816c4d83ad6602ec0af763ee9fdfdff49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61397973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1280d00ddc8ce3338f6fe683c3aac020897b8c18d135f308b5488e0e2847e4db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:45:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:45:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ae12c2ff3fb5df23b854f2a97ab858f54bb2f71491a9276fddf8be7e76d3182a`  
		Last Modified: Wed, 24 Jun 2026 00:28:34 GMT  
		Size: 50.8 MB (50835655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fce37cde330f8d1ae2506c6b080cac6bc79df4fe165dd82321baf47860c8368`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 10.5 MB (10468215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7be72cac78f9fab2e737c59dc780b7780871b6e29b62d1b92978fd80a032dd`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a708ed2acd10ec87ffd95e4b7a78040549e6d8f8f769a9c8590332b707c6c59`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a060711e22b48af24228ac3caf54a75641b66ab5718d4a05bb1e788c298257`  
		Last Modified: Wed, 24 Jun 2026 01:45:27 GMT  
		Size: 90.8 KB (90752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efafdf85f98ab4243649d5602f7551ce71830901a987a21811778e61c90c5f3`  
		Last Modified: Wed, 24 Jun 2026 01:45:29 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:436beb7e05bf9a36c9c3662487f14f0d7e2005841d572a8d23acd7d8b38e009e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcaf3c92b8bf587df181f5aef9534360fd5a075053f337343d1a8988c638878`

```dockerfile
```

-	Layers:
	-	`sha256:538d9c5d1bd4cb24fc78db37bdcea37f03c0bbcacc88e2e509c89980814aa876`  
		Last Modified: Wed, 24 Jun 2026 01:45:28 GMT  
		Size: 3.6 MB (3612152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3b4586065e90fd092c33c828c52a061efd5632acbc7a38512121453cd9f912`  
		Last Modified: Wed, 24 Jun 2026 01:45:27 GMT  
		Size: 16.2 KB (16246 bytes)  
		MIME: application/vnd.in-toto+json
