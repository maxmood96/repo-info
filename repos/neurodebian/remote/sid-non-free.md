## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:401ece9b9b7a564428d1faa0c0d488a0ed344d7dcf45c7f3e2403fa74dca7203
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
$ docker pull neurodebian@sha256:76e9e995f4c4f86904fe10306ac6088227b0f709013d27ebf02bd5df4430ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60150388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e19b5c754f97b7218621a2ad7415892efe2954224c83c2da86a2d5629da1d46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:45:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:224b32b461470cab0a5b83292cf42319369c28ec8beae34418e705d6d0530bb2`  
		Last Modified: Mon, 16 Mar 2026 21:52:47 GMT  
		Size: 48.7 MB (48676470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca5d772c892170c87d0a816d02bca5d34d5f7ca64e714e57c1490e7ed49f93`  
		Last Modified: Mon, 16 Mar 2026 22:45:13 GMT  
		Size: 11.4 MB (11381180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57469f7c59fb0fdcdd0b36b09dad92a22e9e27d58cbb3382c1cf96dea721f51`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534708c7790614b41fccb8d1b06f493d6f53d9ac328099d5fb668761e97f5b32`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e3dbe970409cab1f0211816b271687786f2f5c9fe9ee2102caa213515c56ea`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680101dfe5470fbe3518d073851e4e98819f1eeada5673af5a3d2b2306eb6cbe`  
		Last Modified: Mon, 16 Mar 2026 22:45:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b56c36aecfc51dfe3b41a340b400c25bebcee2404771369cfafb03eeb682072a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d987c886e7cac60b0a18a6cc934fc531b684c3bf9cac481f122b6bf5cd898814`

```dockerfile
```

-	Layers:
	-	`sha256:0d057c6c2a0dbc41f04d346d378fe95d149886bc44dfed5136278413370d47d2`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 3.6 MB (3552906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0c1add2756e6318c73674eac374bc148811486de0b783f5d373ae71030fd57`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:316a56e122edbd573a79a2de5f3d75de2aa40b0f0b076df9cb9078a8924ca94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59885398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af734abdcaae3b6dd42ab3ab31c9cc26f1b6a679b439ddb13fffa3bcae11c52a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:47:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:11 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f8aa045b0b46f2987d2dfdc549957d53bf9eb7148b1452027f1bbe82759ee08b`  
		Last Modified: Mon, 16 Mar 2026 21:58:00 GMT  
		Size: 48.7 MB (48715175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15f2120aa02b76483cbe03d606a903b0903900913698902e3d77a29d7314a29`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 11.1 MB (11076885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0488830adfbaad80a1040eec389eb3dc2bf86fa1dab231c0ed0d3048cfaea46c`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a76c095666fd560b53498568dd4d4d556c26247b75aac3877c0460667b24d74`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4163bbeabab58b1e6d1b1932300651fbb20bdd6b1bc34dfd37cd2713210470ee`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 90.0 KB (90020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8ee29bdb6356fa7c9ff60276dbcec78e12070f393bf1c74149a42761b2b5f7`  
		Last Modified: Mon, 16 Mar 2026 22:47:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd2f9c32f345398ed26d176eda827c26cd495bd913f09b69e8712f2a094cf14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9caf6b1e293c67fff7eaec5ae5f7307c77103c874b33811276b1fff822c47170`

```dockerfile
```

-	Layers:
	-	`sha256:98caa2b25a8ea1717a327cb56dd68e953776d481ec3ab95b60985979fb91bf7c`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 3.6 MB (3559707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d6f034189525baf2b751d1e14ca27f8535e129f125bde3602b992259d4fc1c`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f92cb038c1549da7e7606543cea1b37f5e33aecae18d51b680fe7b2962beee61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61647344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9097946a5841af837fd5d7a4bd991ec34712c47638a936b75fa670e1dafcd2d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:45:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d910d8b21d9682e89de3d97b422096e3120f61049a143cd139a1c42e9bb8b77e`  
		Last Modified: Mon, 16 Mar 2026 21:53:09 GMT  
		Size: 49.9 MB (49948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ccd876f6aa19c74a020294759acdeb35dd1245a040209f4ca69527dd7ab372`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 11.6 MB (11606313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce7e45512f12c2bf1b2dd24d3fa2554dfa01a69158f3f6f2cff4c673120960c`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12592a476099ae3908d871cdb1ce7a4a285d11322d73a9fb479161fb624eab11`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cb8f37b7cc492634b2cb567f2e78dd488a35a98fbe265a251a020534d44e99`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 89.7 KB (89665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07da676b418cdd0f4219b6c91a9b37116d8096542e34b7f98df066f469d8d1`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b51352ea60a625cb4386b46888d45f5533db3f02ae1037a9e158a801320f4be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2baebd2f515e37ebd0dada90132cecfeeea4a30f763ebed5e184ddf44611eaa7`

```dockerfile
```

-	Layers:
	-	`sha256:c38239855257663e51b69680c2e3168694aed9b6b4a98221b20aecf6e193b98f`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 3.6 MB (3550858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc003d177c616b75b01582f33421075f7ef8d520b9fd75e138dca77a7829a7c8`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
