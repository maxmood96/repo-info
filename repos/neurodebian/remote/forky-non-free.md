## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:ed7602929a16feb77c64d999157e6faa174867845d23be61bab915f7fa103912
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:cb78772f90833a757dc6802286e148cf3c5fdd530666ccbac0f50d07cd172653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60159012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2defa8836dcf6459cf443a2e3c73a1fd010958213510f963cd5c1931d8a97569`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6776c7f73607461d5327de460aaf62de8b210cf5cbabd275c1527eff4955c3a`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 11.4 MB (11368639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fbbad51860c6c845e5d68293c56ed4d8041346dea6accc934bfd7afa5b04ea`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d47c55cd565e841baa3ec307cb01da37a958fb06b13982b82d4e1f04004da1b`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bd9aacf74bf4e163d7b40d6119ee3d8d48b3b2cc7078db0ce2a4c407aee1e9`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 89.4 KB (89368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7587b914565a5c0df3372adb2b48d808f6dd8d77481e277a8328669fe85f5a2d`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9fe49f9a5928025f88824469880a77736da4d7fd080ce7922107878270963dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad29b1f5f6319081ccdb52337076454a4d4aadf77bd661e55aaa98e33f4c32f`

```dockerfile
```

-	Layers:
	-	`sha256:b505af5a4b755ede91f3606295650585caeafcd0f080f4b5e6a7ad0bb04fedef`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 3.6 MB (3553195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfe9ebd24f1ab7fef1b09817ad0758a918d9b82241a822a3d85aa1887562effa`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c5f596c4bf8c0ccc478841c47092c4a4dad71a015d664685dc1c4b96dc058b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9528113b20964df2f7a7b1284f55ba0993cab2d96ad5485be40a46fb10c581f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be64bdc407e7e3b95b79a3ffa508782d23c39791fc66237b6b9ac0079e6f8e5`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 11.1 MB (11059006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a038166bca6013ff60ba5efd623dbb4e5fe1ee3d4446048b568c45cd48f1f4`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc2ed7a3a505ca3103c47fba46d5e291e08d49ee72ba39dedef20b1008f326`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a68e5868a8cbc24ca18677d15c10aa94f4c51fb3e1f19e418a98acd77848b6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0446785ebbf74532dcba92825c6decba78dcf6a16420b18506b2ed57f7928eb`  
		Last Modified: Fri, 08 May 2026 19:46:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b0d5416b6794a636e42304fdb74a53a9ee53950b35de114de8bbb04947b6043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bac42a5873dea8825b57dc7136a3a27ca3ab5b4fcb1501abbb9798be97ed00`

```dockerfile
```

-	Layers:
	-	`sha256:24443809fcc31ff23bd314ca750f0f95a8effe8849bd1131390892d2ec92e5a6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 3.6 MB (3561628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a27081017521680b89fcfa70690d05d07b6f2c8103aaa1557dbe8917649d344`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:68c8caaa525fb7223385d32365035d951af0a3cc72b4e66b7d6cfe5c566afb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61677937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa17230452c876a2d8a3c5576a8fd1bed30d1edb5a39ba11ce261aa6798a0b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d662fdb158408b2fedf0e40b496565b70491d8294bf1c490553c3dfda6195ed8`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 11.6 MB (11602262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f78d4a1b4d2014b2edbdb4fccc21825590436c931b9e0f83fb963975b07944`  
		Last Modified: Wed, 22 Apr 2026 01:44:32 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a4e93492a9888476101da3c86d785101e184400f602205dbed1e959478beb8`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81242bb0274bd2fa6ff5b612f329761a3e36e90e6c8014ad4dffb5bbf8f19c15`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 89.7 KB (89686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5455fa89b26cd82935fd1de8324fdd96fd098ee9cbfb2e706521e60b8dee73`  
		Last Modified: Wed, 22 Apr 2026 01:44:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bbd9aa4b5708608a45a6cdd8dfdcd329e96786dbe49d94fc30576bb1a4b36cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af604f7169325a941fea2a219908462b6f83dc4385aab437c6a10ee4b931f1fb`

```dockerfile
```

-	Layers:
	-	`sha256:6667e66f263848cf3b7fbbe831ca021279975fc3afea3506804a05fa97621020`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 3.6 MB (3551145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a30d397fdc35c8ecec80224e63ece1557a301a9bc58960549bfd3070dfebd1`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
