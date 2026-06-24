## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:9a304157578dec578758098d6646a5f95c0a98347218679e7a804a0a635e7fee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8f6e67eb59ddad22cabfd90cd8ec45a061ae6dc5ac0ea1faa813ccef5af03cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60333356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dddf8046beae3a174c8c80825b32a73694fa24d23e03c9ddf5ec1363865271ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:45:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:45:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:45:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:28b937e10116ada256c357287a871c307568d210af49526b0b54d19c0dcdf5da`  
		Last Modified: Wed, 24 Jun 2026 00:28:07 GMT  
		Size: 48.8 MB (48778379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12424b7d15204c997f0543e1e619cea44ed164e28c7e399d70e00cd3aee17ad3`  
		Last Modified: Wed, 24 Jun 2026 01:45:30 GMT  
		Size: 11.5 MB (11461823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc887552aa1aac69e9e791992ee6bfd338f7d5fc9783360002cf09cd34739e5c`  
		Last Modified: Wed, 24 Jun 2026 01:45:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1302ed32c3924147cc379535e88cd353462cd5727b843195356a5618b09ca8a9`  
		Last Modified: Wed, 24 Jun 2026 01:45:29 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a27a4aae0775562680df8c16495a5e5ad2e8014f2e3c669fbd6d3bafe2a862`  
		Last Modified: Wed, 24 Jun 2026 01:45:29 GMT  
		Size: 89.8 KB (89835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd67987a2c84f9758f518013a155a4f76292f9cc6320f3db748c8efcb9aefd95`  
		Last Modified: Wed, 24 Jun 2026 01:45:31 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:40518d17383f342cec85f36577a6c12ef67568622afc85d64f53a98ed1e4675a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59e584810b169496f09ba476dcc6d99bb0ccdcdc20ba8f5aa3889d22d4eebd2`

```dockerfile
```

-	Layers:
	-	`sha256:29db224c4491d3152030a17cf967e9398dde3bc29e48a71d351719e7c65427f3`  
		Last Modified: Wed, 24 Jun 2026 01:45:30 GMT  
		Size: 3.6 MB (3558355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e27e52a4364e92d7cd27e07a5229bf397a2edf26d87b484232d4f001b974eaa1`  
		Last Modified: Wed, 24 Jun 2026 01:45:29 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7e61b50ffbac59dfd9583ba279990798f19b673a00580ffd8f88d7fd6ab0ff8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60042087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8c568d5a30102825cbd1783e90b9fd13889eba73c5bef9f21833718c20c5d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:48:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:48:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:48:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:49:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:49:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4fddf52615bf1690082a9d73cb8346614997b5b51315236c93a190fbd50fb899`  
		Last Modified: Wed, 24 Jun 2026 00:28:05 GMT  
		Size: 48.8 MB (48798835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0de53c870ac2c975727e1e6e262e6c67909ed871769e29804e9ccb5b75a55ab`  
		Last Modified: Wed, 24 Jun 2026 01:49:08 GMT  
		Size: 11.1 MB (11149497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d3a9052c5fc69b30fe247c52919da76b510e8b194c75862cc38d3cc9064aa3`  
		Last Modified: Wed, 24 Jun 2026 01:49:07 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f886bcfe5b666c3b7762dd45748af67744d2c0af7dd9abbf9ab630515245c031`  
		Last Modified: Wed, 24 Jun 2026 01:49:08 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a335ddd10124e4ed92d2e4f4738cd58356c71246207fd8f85f4645668ce34d`  
		Last Modified: Wed, 24 Jun 2026 01:49:08 GMT  
		Size: 90.4 KB (90435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d3cb9093cde8bcb80d597ff70df796d6ef6cb08fd8761928f583af2293f7fd`  
		Last Modified: Wed, 24 Jun 2026 01:49:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eb91629b8d1f4ae0219e52b597a3df99885b45352c670e1271db99c00a52b1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf046a1004c2f9bfe5ff2de9a9cfca500d99fd1c08950d02095c13ff97773d72`

```dockerfile
```

-	Layers:
	-	`sha256:c0a90934088e0b05bcf9b0411f67e2703b83cdcd7994ea2150f3f639e302f38c`  
		Last Modified: Wed, 24 Jun 2026 01:49:08 GMT  
		Size: 3.6 MB (3563060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ea1cd2cdc0c6fa480b0803e55f7f03f46055075aec54501e1bd2c0f475215d`  
		Last Modified: Wed, 24 Jun 2026 01:49:07 GMT  
		Size: 16.1 KB (16070 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:46b7cb8f647a68a5248e01044e099b188dc0ef419c7ec680a19287545fd43a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61872131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76132dff404b68e08cf7f0cccafac943f1954212a6836a38fc29282927d8668c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1782172800'
# Wed, 24 Jun 2026 01:46:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:46:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:46:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:46:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:46:07 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:466f7f9acdfac81cb720fa13d53a50111bee95182357f963947200187b3ae3fe`  
		Last Modified: Wed, 24 Jun 2026 00:28:18 GMT  
		Size: 50.1 MB (50080955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0661dcf0892236c7ad6a3772cd577438245afa6a970cdd7d75f4ef1d4fcabcbb`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 11.7 MB (11697768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3be0d6a535f0f2554e712d75691f577c3cbd2278774bb14085f694f2bb53f96`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5692dc14820ae2b6dc7893762711293c89add7cac576eb143644d4f190997b`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2467b2a5569126a69b9d278550ff2e9b7dd20d11b8b4100e817c521f82962c0`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 90.1 KB (90086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d501b7bce95c0c3115cb5afd3fb72a90428f014abcc10986fd7148f58623c`  
		Last Modified: Wed, 24 Jun 2026 01:46:15 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf5fdf943bf50b822dc9844879bcdf59dba86e72b2aa01f6471d3d0870843f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0994ba1595a2933e6fe9b3c4f10eacdac01294daab404ad95b784879c973e03`

```dockerfile
```

-	Layers:
	-	`sha256:e331e30ede5af8691aafb177ae46b119274b0e1f3d7e03bdb3951745e4f0ba0c`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 3.6 MB (3556311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2c584d176ec5681766d0c02764347fbbe2d6c677cd384d3141c439571a0fe5`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
