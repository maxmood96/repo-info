## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:4fcfe4cc9a359cd5ff6897c80268f988158f7dec262742681f066fadcbc1da21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:73359f39ac469b399641045f30993cfb1211e665c14be5d1be3acee4e7e6c301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d22f295b20bd63d92e469a3aaaed3cafa6fa21e068930c1c9e32c3062f9b135`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f1341f5b046e45d8141cbcd596aeb5bc9e20d1e772a9ff8c5383c022fcef98`  
		Last Modified: Tue, 12 Aug 2025 21:24:55 GMT  
		Size: 11.1 MB (11105055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde9ea5ac798c1e0bae96acc06a9584dd91340b414ab660442644c94a89ef88`  
		Last Modified: Tue, 12 Aug 2025 21:24:54 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959cabf2060cde6a56e23db3803fca3e12d2fba962b3e7fd543fa595528edb9e`  
		Last Modified: Tue, 12 Aug 2025 21:24:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ba63842ce77c124769a83ad2d9f4800bd8ac6ffd41c15e2fd340e76fef3b0e`  
		Last Modified: Tue, 12 Aug 2025 21:24:53 GMT  
		Size: 101.2 KB (101208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ba9e50898a1c5e35cca4388544d0a2e1719f890e357f6f28860c5d91e8c2331e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd631cb693e276a66445ec7ccdd248112b40f621f77658d840a970a06b7aba0`

```dockerfile
```

-	Layers:
	-	`sha256:64570b92741ba52b33cc885a02c68e29729aed2542df7184b65ba4171d288590`  
		Last Modified: Wed, 13 Aug 2025 01:07:36 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b53f8613bb665bdad8ff512be081aea8fab517622d6d961fc62841839bfb2f9`  
		Last Modified: Wed, 13 Aug 2025 01:07:37 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0512689f3cfbe199ee48b6431b2dd258c6955e2f62187e5e56f3492ea6025d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73a205559c030d50be1f5e59a273a1cd3312c2164151863187294443c88500c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c18e7907793e86e4c9b4f54afbc7f041f620e9915aeae582feba6910c5d3fe`  
		Last Modified: Wed, 13 Aug 2025 09:16:44 GMT  
		Size: 11.1 MB (11106133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeec47a0ab1423984373ae0303d9919cdf61e21c670ff1f3ccb7f6c5a0384a17`  
		Last Modified: Wed, 13 Aug 2025 08:24:53 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ecf4827c1fb509243c0b166ea022847afa5b20921aa447345b6e9d65d78e26`  
		Last Modified: Wed, 13 Aug 2025 08:24:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb37c179c91e7838b6ea61418deb0216abf359de05ab1705f97a3867b180e376`  
		Last Modified: Wed, 13 Aug 2025 08:25:00 GMT  
		Size: 101.1 KB (101117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f81a4edae06c09f4a2e3056bac594b088a60586c8695c680c071a968795672a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca203384088fa052de72c03bd7c7ed433bc4cdbf05826dc23942abfb219f4f1d`

```dockerfile
```

-	Layers:
	-	`sha256:0ffb42e8aefce766748d6942b3295332b477e981dcaecda86bf239903e0e1d3e`  
		Last Modified: Wed, 13 Aug 2025 10:09:38 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c105b04a40af2902e00525259dced98e10358a646c041d729301d3fdef42df5b`  
		Last Modified: Wed, 13 Aug 2025 10:09:39 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:545a320c35566a388f6be80f1e52cea27a8e1e2c37c04ef3f3cba5cf7980f30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66294246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74816509a8a58a4184fa1436229bac424666f7a54e88b1bb15d18559a5299a3f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b148e76c29cc0ae2d2cf6449d62900f5cf24990640523768d8221eafa133979a`  
		Last Modified: Tue, 12 Aug 2025 20:44:54 GMT  
		Size: 54.7 MB (54690594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017e1a7b0b50fcd0e466a61f7a7b4d4a44997caf469d94b03e7f2aee7e60d844`  
		Last Modified: Tue, 12 Aug 2025 21:21:05 GMT  
		Size: 11.5 MB (11500388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1045fefbcd8ea997c7d117781f2b9b047731bc82cca186a8828f2b890c6c8f`  
		Last Modified: Tue, 12 Aug 2025 21:21:02 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9fdb56429033d88ca09cb3a5efccb8795a9853cf8fda42dd8c0dba2f5e6e97`  
		Last Modified: Tue, 12 Aug 2025 21:21:02 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558427f9783dfc4dd7d0c4fa214ca7c5dead3b2fc07a136d8fe80f6cfc873969`  
		Last Modified: Tue, 12 Aug 2025 21:21:02 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6471951e91cd6844a74b6ad78c16ced99ecb938d41b140a5fad91093adfaf059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c338bcf7d1b135dc0e9a37708d9f9f49adfabb59550a1248cd9d393867735b9`

```dockerfile
```

-	Layers:
	-	`sha256:7f29d7bc133c6847669f72eae2ead5f121d1809686d86a4ddbed7862cab1e23d`  
		Last Modified: Wed, 13 Aug 2025 01:07:46 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7b428175076bfcdef56cd8244e4c727bee57bbfe6370955d357d32a95f6802`  
		Last Modified: Wed, 13 Aug 2025 01:07:47 GMT  
		Size: 14.0 KB (13980 bytes)  
		MIME: application/vnd.in-toto+json
