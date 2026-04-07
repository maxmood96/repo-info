## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:24e14e1b58a1807440bcda71183138921fe9bde3590d423cbe3440c61a75259a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6a97ce654e0eb6552d2bb76efc3454ead70afe0a3fc2fa654673e187757038ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60172027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a82e705f83fe881c5e5f192d8010788c9bda962a056898feb36bb82f4f4b26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:01:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7b208148f3abde07a5ac47cf579ac1ed4c9312d2ae485addb285765d8008fe12`  
		Last Modified: Tue, 07 Apr 2026 00:11:41 GMT  
		Size: 48.7 MB (48710648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e359a898b31b0e9c8c58f608eaa36be1b8c82ba572cd885ddc5b74e54fa00d6`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 11.4 MB (11368694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd15120090ef6e6a2c1358a10ea832b710c945b4d206662782e92c9eb53a2fa`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aad35ffc48f0873d152bab616af660e071c2abeeb01fa91ce78f73e038f5db7`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7f82a3b3c524294cb678870650f0f1daf178c7144dc185a3d53d63e878ebfa`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 89.4 KB (89363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f0c8526602a286d241f56054e7a00313cbc165ad25f708608ca9977783b8d`  
		Last Modified: Tue, 07 Apr 2026 02:01:45 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b53f533863a2d01b3271f410c55bbe4efb865cbd221fdbe4302e9cdeafd15e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacff77bbcd6b5fcec98b0420bc413e3a4f66b7cd8564c4a2ae88b63cdb57a66`

```dockerfile
```

-	Layers:
	-	`sha256:f57d844cb34d7a636b5e7f9214efc0f0153dc056af5e3dbf29c2f46a067bc9e5`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 3.5 MB (3549123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beb01c446a636d846ec76ef42de8f855540cfe404fa11aaa94e5977b15beae3d`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9c61266570716a76fa4d66983ae408d5eea38ae55812bce1046eaf473ed9b647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59910666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de0c61091b23a1980030577b83f83fabb42b6738b3662f056ef9049f88e3748`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ac9c76c00b1b19d9057c64eebc87efd57976d9d3d4373752703081335cbb1900`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 48.7 MB (48744945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85840404f57afb5787eae44f30186f8ebdedf22f7341260a6d562a2e16e6d27f`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 11.1 MB (11072472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf44374b898e8eaab4fef95f90b0e127e4f6eed7b5bbf963f568241a8fb2e36`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c14cd1ddb0b2f50fea0a090beb46755df524ebce2f44860805c804bada8407`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7c94331ed393d89b3a0b7e290ccb642a59a75c1f15fa8c5bf35faa73cff651`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 89.9 KB (89925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38896d5a61d5211f6261adda86c26527050e97d2538d0838ac55c5cecec9002`  
		Last Modified: Tue, 07 Apr 2026 02:04:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bac54ec2ea8eb1dc276e26335cc80a4a48ef1c43293159e45895ff1de30d0bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b089d25c53dca863e9b1b12b678ab6f783254e946af06e2e5f07ce7f16f001`

```dockerfile
```

-	Layers:
	-	`sha256:25c5712129944c709b840f4168586b4a685e4b2c4688d661d19a9dd73dba8215`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 3.6 MB (3555108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f09c4d225542d79fc824670a13b384c9c0686035eba21c64e7146ddff3ea29`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:379dd6cda62c5f956daa4957282d12057faca8d0d2edb10eb00b63aa4b127649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61688954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4690074633fe4fccb4c59a578a84a38bfc055cd41d859f3fe6750c62c03075b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbde13ff2785b11cd70a92d1da45b61ee2c39ba77f505a32b6764e1bb1f3464c`  
		Last Modified: Tue, 07 Apr 2026 01:48:59 GMT  
		Size: 11.6 MB (11602276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8a43f3df2ec92648d7f9cb6ae9b59596ef7550e9b2c0de212a9d5067d70eda`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8292b280ecf08c2a53b62734b37ab925c0596e7c8837ab862f48b6ed13161a18`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4fd33efcb827f079f283388221dcec47472439dd679e48cc1dd8c9c469c885`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 89.6 KB (89646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee066862e919913f4a8149190cef898dcb0dd51f675a1b0b66cd695eab88dc5`  
		Last Modified: Tue, 07 Apr 2026 01:48:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20806508b55568c0a85953b30cecd0be318bf1353380d952b6c350c1f23b2cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58350dbd42299c78510c7b6d6e14c04f9e9925d1c2ea28148368a9e35ce4182`

```dockerfile
```

-	Layers:
	-	`sha256:07eb593648572153e5a66df88d45281816a4595bd6859d58ff20b91cf3e389b3`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 3.5 MB (3547078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60adcebb1386384577e15e4ca93b84d41693ee7655e05bbf56de36d0fc4ace0`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
