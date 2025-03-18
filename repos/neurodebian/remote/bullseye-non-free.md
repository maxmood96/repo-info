## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:41b89a804704044690226b9a583e897838fb160e0721cbee6197f00f38840c57
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
$ docker pull neurodebian@sha256:cf5a94ff2684dd6fb4f42d88b70d909325820350dc5bfa3987b3bb4eaa7c2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64950083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a517de29675a25d6b150b4e7b4b4fb0556d110ebe7a17e5484da2598fbaf9f0c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2128041edefc21398ce0d5d3e76899100d6111b14754471c6d57f6a95663302`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c911d4b2a647f09fcd0f7d3123491b76d4f4d22f8b6bec25518100d70a57bc`  
		Last Modified: Mon, 17 Mar 2025 23:47:30 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dc26b815c239ea7046418983685fba99002caac1570fe5ab8402e2baf7a6f6`  
		Last Modified: Mon, 17 Mar 2025 23:47:30 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe7980f9f45673702f0ca3f64b9da7c16958ec20f7eee42617328db1d0c5a16`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 101.2 KB (101200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a2e33785086265a4120ee2984d150053ff7f5bd0a7127c08021bbdde63a76c`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2af51f333f084a579d2a0e89f57835cadb526772903e96f88148caf2f715fb49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df31889e91d31841ea2ac95334c46b6f4804f8edc6592836cdfcdf27becd29e`

```dockerfile
```

-	Layers:
	-	`sha256:15ac0ccbd5914f2350853897dd95b2cb995675721e33d57376a35a0052752f63`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1644d5174dc242228f6c170e8c6ae8d7fd7b24de1fc0dd060787f0b3099b0dec`  
		Last Modified: Mon, 17 Mar 2025 23:47:30 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d6450fb3eb05129d4687c51bcab5623db99b785f0cbabd26f700c155cd2f2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d72fd46840fa0ac12e330617a792486e696c49775a791c82d144262a1e6175`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3882a7dd0a14bea13a77df5b4c510fe24b4731e60a214c2419a057b09f823`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 11.1 MB (11106035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee718847ca2a78d990086602ec053fb4093415d671b15ba9596f39fa04bc679d`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76a051cd4309c8457edf6b80401a713d6d6fc6449b6443891af1c92d43911af`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70248da80d442a8395b2ec921fbe2e7bcff12b435112dcf248d689354adb71cd`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 101.1 KB (101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af88f6b11190973280cd1f0ac3d93baadb144d0f78c29bb98f505deb764d2d3`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1359592cc092c24f8d650d5ce33d1e228e369c87aee73678f04271eaaa724d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3560fa229acbdb21f7c5819ee3defd03a0e18ff294bd4d6a4390ce156296a272`

```dockerfile
```

-	Layers:
	-	`sha256:b82a3bf24a817f178e6ff2ea7d9f041984143cca6d6e858d9335352ebd17371e`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eadd77ea4fd34eaf2d41afe92967fd20a98c1f00f41ab16400012ef4dab2b9d7`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:04f9df7957f7dd163d8de42d4bbb6dac2d1a9b4e4aacd4316b2e50ed99400644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ae5c6f991141be1313e144a8caf7b593c67a1960f7e3198738d330df3cea1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc3b2414407ee0ce5350daa8d5da1bc6a5e939777bdd0d41aeb9bcfc797648c`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 11.5 MB (11500353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8587a5bab6d44a420b50e2cbf96cf850b46c789149389f96adab1071ffa8ab74`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93102a533e7b7a65f775355be41fad351dd2e80c845a717f5b0939fd329395ee`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fe725953d5b29ac9c6e4edd57bb7453e54b9fef0b1993732b3d15f2848c1d`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 101.1 KB (101101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ee16d55a900518b9e036c04783e292e4d56974b53d3ed282278af3f8d09352`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b768c2edd91f9917ac196859b3929fc6f2f9132f85b71f2eb9c4cc4efe9bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1128898b329d434fb29e99f07d32f9cdb44c00a4711fe2a96488273c9fdfa99`

```dockerfile
```

-	Layers:
	-	`sha256:faafd4cf4c21575ee9f0d61ed6bdbaa6b10dfb85f631133282e111fcf6468373`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410f6ede58e127554018ce70ec907278dbd708226b3e7961b5f72e0542a41e29`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json
