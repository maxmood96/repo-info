## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:e0a8c5d010350e97fe5ec700fb8e46ab99a1261c5ae5c3fbf1e311be638be86c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2aa0ca06e51bdd6def23bed68391c7e0d6ead578eb9de32989b1a85acd5c236a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59871659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ea9b76dba2e9dc94aaf168e7ce1f51e16e46ed2f605ed463f95f45cb79dea7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:44:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:44:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a1dfda4a8d502c8b1d8ad662984c80cdf18fc78e41d1fc3e6bf60e8e378d3f`  
		Last Modified: Wed, 24 Jun 2026 01:45:03 GMT  
		Size: 11.3 MB (11273419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82b4bc40dbdf3fcd19dc69048ac1535a98ea7dd166fbfeffbf8fcd81f5ec109`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76f04601659792715e3715a468dda9e5bf9458f720443682faea1f1acf999b6`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6087b125fd2e47b7c4e64fcfd09805011d62ac94494f538885e9754db8123a39`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 93.4 KB (93412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e673663a5296b585b2bde5722fd847c9e854537eae1af4af619349383e1829`  
		Last Modified: Wed, 24 Jun 2026 01:45:04 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0569054cd5481a9e85458e6e3c85d8011b3f99b5667678976c6c28a5c69afef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4081b10479d2eb52745a28964cec3320251e8bc8a65db022a7e705be2e26cc`

```dockerfile
```

-	Layers:
	-	`sha256:cd4b71eb3a01537c993cd756caac493ddffa5d919c968c4ee58205d37836fa84`  
		Last Modified: Wed, 24 Jun 2026 01:45:03 GMT  
		Size: 4.1 MB (4075951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e22cbf4232c4e2019722f1b0983fb76422bb204cbba14d65c71f63f8ca20be8`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 16.0 KB (15991 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ff2802bfadec3407144f37eba255b77f364237da31d8b22943e71ceff1867e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59738341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725dd8aa12fb0161049b76fff8d404d979ed5e34835eb7864a6af7a0e296205f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:48:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:48:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:48:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b57f8b6430338bdbd253e67f1211778a3249bc19b3d337b29b7d77f4bd2100a`  
		Last Modified: Wed, 24 Jun 2026 01:48:39 GMT  
		Size: 11.3 MB (11252936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17449b4c84b5bfdafe2b666f8f92ea0c7a17ccbd33d13c2eb66b2ad76f4208a`  
		Last Modified: Wed, 24 Jun 2026 01:48:38 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef7adcf92c1f89331058f54432cd0916e434637f5350b994de71cf0543c9da3`  
		Last Modified: Wed, 24 Jun 2026 01:48:38 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c85c01505091d0017cfc26b5b19103aa4f743f49d33df9be6dbc15b60b7a0a`  
		Last Modified: Wed, 24 Jun 2026 01:48:39 GMT  
		Size: 93.6 KB (93580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b6a07115232dfe8c8c8bbeddec00e69552ac6b8ce225312398ab28bb6a034`  
		Last Modified: Wed, 24 Jun 2026 01:48:40 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3575ca857707abba734a2542b5d9cdbd56852ad914143ee1ad22f9d070fd2d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e6ded0e3c7666debc96f5f36c1eaf6ba4d6657482c4e1b3213b5cc3fbbc87f`

```dockerfile
```

-	Layers:
	-	`sha256:d681fd95442c46985aa5c0598999538e5eaf3e6a55544eaccab0f08e5e8a86db`  
		Last Modified: Wed, 24 Jun 2026 01:48:39 GMT  
		Size: 4.1 MB (4076193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa81045ba757e5ec483d14cf83519eb057221ffa30eabbb18299a536022e0476`  
		Last Modified: Wed, 24 Jun 2026 01:48:38 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a8b501055f1ee1088e65d5a8e82e588192c54432ad10ca5846c7afcc93fd2824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495f2e3d7f18ff4a2a76585708f8bb4c60d8b2672e5e98bc3756fcf411afd7c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:45:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:45:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:45:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:96cbacad9c1883b9ae87f68a0550ac0bd7e0b7ba2b15b142a793b89b5a5f36ad`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 49.5 MB (49491378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de7c6a2bc43aab7bba927950ce09da24387a65116705f1c1905ebf8a51d1776`  
		Last Modified: Wed, 24 Jun 2026 01:45:13 GMT  
		Size: 11.7 MB (11693079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb973994433f14f5335696271a5bce15ebcc853e5d89b15b07c8b38cff33b0`  
		Last Modified: Wed, 24 Jun 2026 01:45:12 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee857f661b0cdd38b84f2718aa65773e71cb5558684ac802533e984748695c94`  
		Last Modified: Wed, 24 Jun 2026 01:45:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a76d5905f55f0bdaf6a41fdcc8551b194ad190fd0a589ad5dd868056703bb2b`  
		Last Modified: Wed, 24 Jun 2026 01:45:12 GMT  
		Size: 93.4 KB (93445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b41b61def5de9a066396aeb093d8d960241812a072992ffb9e9cac423dc2bb`  
		Last Modified: Wed, 24 Jun 2026 01:45:13 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f4e0e1f19b016a6a7369a0861be92ce0a9bc5608eef11a8d5e589b766e0e5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011423bf913ebe70f934c3bef6e76d8b8d7071dba083236a48f3cad9c36394b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d6655f756adb753001781a23b4bfd1975f332d1b4e7c4e4bcdbb4a16330ced6`  
		Last Modified: Wed, 24 Jun 2026 01:45:13 GMT  
		Size: 4.1 MB (4073918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49454077d2a18b47b0b90e5b2eb932a8d4f9c4e915c402fcdd25b0940dc95a5b`  
		Last Modified: Wed, 24 Jun 2026 01:45:12 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
