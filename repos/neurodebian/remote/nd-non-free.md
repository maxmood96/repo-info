## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:244ceb264bcf03306877999321ceb7e02989a73bf95ae57d5ee85e72e1028e30
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
$ docker pull neurodebian@sha256:b5fe02ba6e80b840d27c9a28023093ea6c23d0c9f89a31872582dae4ae70095b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60197932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8a8113f4d5f843d3701212777122250946f4084ea90c4b210315d8c8552389`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:27:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6e71e03194020c479ea6543a7f33f5099fe2418b16c8172dfe51e95cc37839`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 11.4 MB (11393195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bc269137e2d1ef84e9a7f609fc3cee05da2a89706f759a7fb1d61120dbf448`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f9d3c942e826f99ddc6c49a7e3b652962a818c4f1d9922b0ce1742da0e16d`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a46f5f08e788d4c601b78c2f74ee528b3e922bd597ddc3a26614d7f0b61435e`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 89.4 KB (89401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0712a6b21cf63c1f33a22eb08643b4e391abf913201dbb2729f8ab5e93d38911`  
		Last Modified: Tue, 19 May 2026 23:27:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:07e73ceeba01283e1cfdb5acd37480d6a18e0c497846033f81ddf4428ff6cc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ea38aae25cdb12c25b7f88c9a1dc8d8fefa9067665af128c4b1e7ecdc13749`

```dockerfile
```

-	Layers:
	-	`sha256:aa9aace3b47fd65d09b268c1a1a0179945bc17f6958197bf895d8106b13fe493`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 3.6 MB (3553400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa2070502a6c70b838ddfe00d5321fddaaf3958e9305ed560c66aab2560d3a97`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fdd6f83569e0862993e48832d03be26ca04c8faf222c5bd056f0869665a221f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59923995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b961227030f6ce3ce85d3b4a28a1bbf746687c9a53ffb5b287e67a7c7838889`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:31:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:31:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dc44779cb8617743124f685b6bab6ed6aa724234cc4ea684ac0e74eb53ffab`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 11.1 MB (11093028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0b4f7877b91c9ff52ee44f9d75b23d583cc18625559b238ae0ad4ed4ddabb1`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c6c0d651e53ea292ef5612a941931757712de6d1e19de433fbcd7cf87dc2ac`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2e9ab7191a3546247ec4390d48df26cfee47a530af5bca3c34d103849864bc`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 90.0 KB (90034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fae19e42bd61f416eefbbb0e6fbb41a346ae78fa1e9ae01b2d2cff5fc1ec50b`  
		Last Modified: Tue, 19 May 2026 23:31:33 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:edd41d5d71718554898395d73aabbabc52399729a7bccfa89b3a2487b861820f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccf3bae28acb19d66c068d98778afdc4eb4041506e225e424b413673506b68d`

```dockerfile
```

-	Layers:
	-	`sha256:10da892ffed892fcb2aefbf7a1af3177eb97af944f1b959a13f3ac0f0ea0073f`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 3.6 MB (3558105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986de3b52a66825431d3fdd5b0cae2b54b16b8db36ba5742038cf5719470dfc2`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fdfa585524dbca77dc88c79d28594b439056998a1873b0734100d0fbfcc4983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e746d8a97559c27eb06570b8eb5bf7fd0656d5f75194b377aaefd9ce7fea3f94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60950ea8f81eeb40f4ffd4c9eb5344310a3d3b4a3ba10d8636c3e11c143743a`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 11.6 MB (11625857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e999e91d392ae0fef15aeed6175ba39d08817b5593d30f26ef16d1565d28f379`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208859bef58c08283e7c0113598e89b5851cffe3ad75ec5cbe4f8826bba0007`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec1337df25fa89a088252f15b64bba7bf8f37501ac5944f7352dd621c52673`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 89.7 KB (89684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354222966e2e2c36cd8e4d1a765f5ce435c85024a44468f4c76ad662da8dbe34`  
		Last Modified: Fri, 08 May 2026 19:45:42 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:efdcb503bdb440864d0bfd5fcf11ce13a5bcd3ca870806e08019df74f241815d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77f0b27c9a0833de49273eb014ec6b6900a97b4265c8339e9c8422a12a57f18`

```dockerfile
```

-	Layers:
	-	`sha256:d3ca879e53a051396232cc6749a325b48a90a77b314898d6642ff4a75b84707d`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 3.6 MB (3554216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bf0aae2c3093143415998f808232246df063b6a5a9ac0bd9e4a9bd97ff539e`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json
