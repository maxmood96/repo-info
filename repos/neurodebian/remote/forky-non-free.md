## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:9550343ea0453f33feee4c83335d02469ffa6f6cfdf7689e92ae44929590402d
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
$ docker pull neurodebian@sha256:7cbcb2018dccbc119decf18339c40bc9fc736bb14cc8d74e98c825cce5b86041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d0d88329284af82434ebccf452c75e6628d4559605caa81af6af292e170fd7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744a6b4b4a9684cbb11e9ecdbc9ede0197a160227d21c42838cc3308c6b4e0b9`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 11.4 MB (11382299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1875139f86f2f68b13903493d1a046622fa09ce497f13444a0e1eb58b29425b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd243b08ecce031850e503074d833e0a24109b4960944c53a4557e51408d7b3`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3886fee5d02b6836fd7bd2c60ebd980c0e65314ce8565e7d96cf232f1071be5`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 89.5 KB (89547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e3da227b0dea7161d8bfd6d2aff718ef57225df903c4973ca36f2fbb71beed`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ad337e08555537483a7bb9dae015c1047c32d396af9afa397e1cccc55def0d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab46e1c1cc371b35e4b33ebc62b0d136edfb65dea896fbcf39af8d63b9571b`

```dockerfile
```

-	Layers:
	-	`sha256:f1b9bb67f26a56f3cf50f6861586522053195a7d15f848f0b445467dff782b7a`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 3.6 MB (3553726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f18dea4b7f0760b82dec582a851fdc534073ead289296d607451d97474b8888`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:677065d982d885d27b4eadb807570b22f44f2983db1ab259f5341e3f6e2247c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59830109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17fc94e4ce0bb45d3fe9fccc40219a8557e5eec5bf6c293554d5bfeb39bf596`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:47:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3e975b0fee3e37d66bd1496d9c27a06cbf22bb0145e1a1b09c557d7dd58e25`  
		Last Modified: Mon, 16 Mar 2026 22:47:13 GMT  
		Size: 11.1 MB (11077490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404e6c74fa835fce831866b24267ff623333e069b8168d66628b785bd9746135`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d66d0e5643e22e5a105441040f5129d783e8cc3c759f5762fa7d9b9c1a9cf`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2ea8027d0eacfc714d35030b0534a0dfbcc40cdd15272c2198660c4b64bce2`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 90.2 KB (90204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c39b8d27f969e6e4b7616e229fc92dd58936cbfc8e6f93f70c51a16c8c36b4`  
		Last Modified: Mon, 16 Mar 2026 22:47:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5abc3a2fd1c35885ac1080ce17113e45a566e09a424e06756036089aceef3ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06df2e2f6f779a1f3b7df9552310fc8ea62db1865f702b4be4b5fafbc8f0cc1a`

```dockerfile
```

-	Layers:
	-	`sha256:6b649bab6cf90da66935cd04a8fc3c09c874fc12a51043877827c9b4377ddd74`  
		Last Modified: Mon, 16 Mar 2026 22:47:13 GMT  
		Size: 3.6 MB (3560527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60edffc23fb055179a0c8e87f176083693296ef6458467bbb282edb5a806551c`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 16.1 KB (16098 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:80b364add1af2faf7bc55958460e350bba3e549e243e3dd8f54516b317d8748c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61618521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8358e4bad4f20174ba84ee3b8c7e93ce05e151ddb68138164b8664a2567b4f0c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:45:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30659db903268f5dcdf0fb4eae9842869002328cea186cb0491a50b2e3232e12`  
		Last Modified: Mon, 16 Mar 2026 22:45:20 GMT  
		Size: 11.6 MB (11605539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a6299c767a6b8de3f66fc6721068e6b86ace4c45d34a389016404c8cfa0778`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fbd7ef8ec04b0ac885f12960dcbfd2785562e6a46c1c6b4716ff40129bdd31`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca67de4ee3edc48b043ae4ddbf1c9677a3815215d1b2ff5e195b2daaa8f528dc`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 89.8 KB (89760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4595f94962f4c142429e3ca0eb002960df4000525b0d2e60c463b0f91934477e`  
		Last Modified: Mon, 16 Mar 2026 22:45:20 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c68211d63100c3a2c47090cc28977f44a5434ea9903be03f237aa1085b09292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61c20573f9eed374fda7260fa480dd9599fb4041f80a529e8886c86ad2d5c85`

```dockerfile
```

-	Layers:
	-	`sha256:7c214acaa1885f2699e93564c144ac761cbf5feb7121bdbdc1c20b0b47036251`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 3.6 MB (3551677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308b361b3a3fd980ba8054456a0fecc5548431fdfadeddea39b63351eaf39930`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
