## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:b44b5529fabf774a6953c7810dfb0a7becd318d5e07cacc59b1d5f70b3e9db13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:4ebd736271d09525672664c3c407e4571dc1b3e4b5456c2f9f1cb57cea432da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59689076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94042a90a21d39fa810f29af2dbe6e9e9e6acf8e9d4d4a0548c07e815ad85df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5ae048d466c70689a7edc5eedf4cf1793ffee4a9b646f2c5582a319d9f8feb`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 10.3 MB (10293020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f3d32951cca7431a1cf21e1aafd0f0fe2b9862713fc19ff35fd5aab0770fa9`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0afa5be5588e323635ba7e46523fcc7d695788b8c883106495ce8fe959cbe0`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d615a8943f123da71966af78797d000d0b087502770705ff702fa8e4d72de499`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 90.4 KB (90383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d1b8a4db5664e6ee8564db8b48db1e602ff4076af3e42b0162ac45ced4d869`  
		Last Modified: Fri, 08 May 2026 19:44:50 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:988cde20d5d12bbbb0de2df64351abef2e21260c34d79bbcac811dea876ef166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c96707ae5af4e3a90694b82d76bce82726327aad21d64f646e786b574b03d1`

```dockerfile
```

-	Layers:
	-	`sha256:97516c0a52ed039e6b3094072fbf6966a275e16ead77e38af34979e8a923b720`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:100674fd8708b6042e678d39193d51e761bba8a6a49fed4f4aceb77bb7f8f5f6`  
		Last Modified: Fri, 08 May 2026 19:44:49 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57b13c1e50963a6187b7e20ca9c973fe30970f06aa206a968c81ed3e3aea7ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32a80663dcc17719bc1935a712da2852657de51fc94f60eaaa9ccc05276764`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77348ea04670cc60ed3fd70e8a942379a3a778401a47da14bddddaedbbcd473`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 10.1 MB (10077993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4f986dcc8620c40bddb431aed2820d258c0ba86a933a572cfb5aea1b7c8d1`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484764866e70b0d12ffdf225ed2ef6dc9af0cfbae6d1ffc072bc54f2bbd8710c`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13df355aa2411e3cab96fecc0b4927c1a75301419531a535765c87be27bdcc72`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 91.0 KB (91046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb102d2bb0e4b299a1747924f034d561048a35b0c3ad22fb08df099037f5e1e`  
		Last Modified: Fri, 08 May 2026 19:46:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a7fc429753a5755b5ee64226c7038ce723951b0fe08eabbc3fba8e4a1697e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c66c6f71d2cc072b4de445c3593012348006787233156dcc732fecc292ecf16`

```dockerfile
```

-	Layers:
	-	`sha256:4d3e70240cf4968ed03616db1c20e456abae7c75f133eabd39d8fea05bf2ab22`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac819a829dd4e682388cbb13c01e4c3ee1c2e11f1c959436f84e286ee2fb631`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b75946ef52c181c76c2e00440d05d0622edfe6da94570e49ddae38ea079dd3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b263265c43778c4c1b4e8f75212dc86f2c4bef41fbb14feea9119600cafa0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4a335a9da7e3093e947b7d57025190b5739906b8bd558a221a15ddf6aa9ee1`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 10.5 MB (10467127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b54ccf8ac71030c118f8ef845986b5523b82fed115f87119415e7d8cc6a7e8`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfaab1b9dbef7720bd0084cf9e3eb661688ece913432774491e5c8964364e34`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a31952666a61c2db472bc221ef5ccc404ecc5d08cea8a1059c7cc6d24e1f2e`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 90.7 KB (90749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a9d9d9e1e36df62b6a57b49fb8a76a463da0ead6d8b53ad51fe669976c35f`  
		Last Modified: Fri, 08 May 2026 19:45:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2acad64ea16cc709a06d2a5aee32e9877e05ebb94c5c760a32e21c3e45deac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a59f41855cbbd51dc2e3c593cbaa8adf474717a361518cb3ebb5186e2b4760`

```dockerfile
```

-	Layers:
	-	`sha256:0d1f3edb3bc163776717dfd578079bce618888a806181425e93980efaaffe421`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cb1f47cd785673497359532ec8428f026e1c4021584f5b6423cb001e8a911c`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
