## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:173e30fe52835888cbf4c99df3681bab5301f764a08471f527a470f7b237a072
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a8fed007c8ece885918c9e11779506e9f53922c5e2949b9ca3d5cad070d8b59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64969912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc48b40d449a8162e5f1e31210abb1ca26c35c25d0d11be4114f8e58602bd07`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad505f834efce27668caf523e6f7448c25363a75b4134fd5057ba74e4a880f8`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 11.1 MB (11103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057dc6f686aa3321affbcc43d99644be568bfab4ec2debf4068d340c0fe9029f`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69924f4323530344676ca0ba491486a80bffb06e2262fc70becf9e9b918754f4`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7b65db8ace6319f2e3e23625af8178e212141849333549cf49d1afb74e287`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 101.4 KB (101395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655b7532e2534c4429e9d72442995afe02dd506eaa62f099f5097faddef6d7d0`  
		Last Modified: Mon, 16 Mar 2026 22:44:43 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a64fc4a8efe1f1b76724033f8342322cc816569ac7873003e430ea62ebf89f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84027ad37af861b608a24512e433b6dfb683b66853d9daabe19988fa537aef3e`

```dockerfile
```

-	Layers:
	-	`sha256:57129e95b5b1dfce52d22fbd3e4bb836b30c3a36cbe4ff668f233d5a627f6886`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc663e27c326eeb5745957332a05e5b6c071d629e203f62860b58495cdfabcfd`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b3a079b4075c5dabbd9b4abd11084af8815b6a49706ff5df1c398180dcf9dec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63460850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e14712e78dbc88ed09b97ceac1a4c1d1d8f90e0fe337112d982d69d86f22f4c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:46:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:38 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adba598ecaa898b7707023abdb9f68145125085d73ed0cc1e498b5c984cf457`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 11.1 MB (11109779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d292cabb5911ad56587ec971725c7bc8459bc5ea9d3368c65846e3764554a4`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7147b26ebc688bad683e055677559613181297547e040d516b7a298cae685f64`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be5dae1440567bafeefbbc1fc1b31ccfdf8a18b5038011af0c818813bf99902`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 101.3 KB (101268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f162b4fc51a4b5b479b1d18c642490d538aa92b39111f59e9de89331bfbc6541`  
		Last Modified: Mon, 16 Mar 2026 22:46:46 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a1deaf99a1978179d2852d8e7d6d5c1a826e8f10683d72fbc6ee379cecedb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f5bd82fccd9e2cc89023f6c7473564d0b8cfd784b3cee3c5fd96cf67dd6ed5`

```dockerfile
```

-	Layers:
	-	`sha256:2992a167cf67dbb060f8de6402a3ec5cf20427aa64cc3bda5b5b202aa51b5884`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360c775f2790a7ac33ce509443166b7249b5d1cbf414208d2f519757f59b24c3`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c2065da5b7c31855e11ab33e080379390113d959c865596fb08c1625c5f405a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66308049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d277798773164af88f8295a170e4711f25a7652e356b5512087570c4b62fe3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:12:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:12:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:12:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 23:12:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:12:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ad236c87f3ff6b413233974bf5899e332a9ceee3a606736011b98ba6596c59ea`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 54.7 MB (54702245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eb604cb66d26c3ee380b5e5770348a3fae759d8cfc0679ecd062d987b54a46`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 11.5 MB (11502008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc0b67b2c1547b9571f8a7988d17e001f4d68d9480f47e673256a3b7addae0b`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499562f5e1891ef1652cdd21ba8a3cae36324fda667a9a9e67f8f5cc2809b7bb`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f8aa7e057a9429c5ef7ca9093b02acc14e6aff4ee29dcaf5dc91570d02be5`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 101.2 KB (101249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc224a67a94f5073e5aab1ff260a71585c62c1473f97dd9862feba1c4ffaa99`  
		Last Modified: Mon, 16 Mar 2026 23:12:54 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:747588784e187ab85736d0525eeac59868067cd98940bbeb78a03d499f8104c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c15c128b27829cab9885becc338a4b19d1d8af4a5aa62eb5675200088378bba`

```dockerfile
```

-	Layers:
	-	`sha256:ebf0118d435c51bf0e581cc838c229dd9ca96226c60565d31b430c3453c35197`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:240454d82d04734ac54e35d69828aafd5e4128fdc67a301c7dfd2af44286e651`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
