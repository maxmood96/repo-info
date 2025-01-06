## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:76a4ff49a40e80f5171d2a53a38c15ef39cb275873a9255c0b5b0a002127aa90
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
$ docker pull neurodebian@sha256:51b5bf21534c25285e9d4139d34d90ae22afc4df81dfb347e8b3d7e144850132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704a3669a3ed5ecee54ca2aebb6abdc6228413eed17023ff52d0ff4e77c5987d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f392250a6120024a6f59fbe82fa68ac8f53e7c1e5f411683a8959bf0173b465`  
		Last Modified: Tue, 24 Dec 2024 22:28:15 GMT  
		Size: 11.1 MB (11105105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf56865f2d4e9edd1d24e2990f89c7aae22e386899b5b021073b358970a1743`  
		Last Modified: Tue, 24 Dec 2024 22:28:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde73eabc9089762be1f68d64c1bf5513d96490ffac1217f2442b11282ec1076`  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2e0583d46a644bc0052d70e5fc109eec51e4a473e18e62641872923fa0c30d`  
		Last Modified: Tue, 24 Dec 2024 22:28:15 GMT  
		Size: 101.2 KB (101202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:38d5242a495a82abc4aba1dfa83d090b2df9353ce487f3862c6ab3818df7d341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7f93b5954334e265a53c44471064a633394cec2ccad0ebdd279a045864f2a7`

```dockerfile
```

-	Layers:
	-	`sha256:cea5aff2e72b4c906af18a1c9224fd851860d650bb8fefa1821ae31df6ea8333`  
		Last Modified: Tue, 24 Dec 2024 22:28:15 GMT  
		Size: 4.2 MB (4232796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28ace802cc48e21435ac96628e0636016872d8cb3343d64c50d6bad48f0985ee`  
		Last Modified: Tue, 24 Dec 2024 22:28:15 GMT  
		Size: 13.7 KB (13692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f0cf56af4f4543fe0519584926972c290c419f235131fb1332ba0cb1d546614b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63454716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa448ec91fc2269f79416ae2ebb2a56c279a9dc283b5721b3267fcaace48dcd1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3fd91d26138d9aaab80f425987de57628c24f81aca2727bcbbe870f7dd5c3a`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 11.1 MB (11105941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d41e172cd8c296857603d6eec38de1b1fcad65483cb5e3a5c165772ebbc188`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583285aa42d4ba42549ac2e4ea57d0849fc285d04fffe2155b702638dfda9ade`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2a8e49cbdd987bb7224891093e38a2baa58d5a5b27980b70b0c710e3e4f973`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 101.1 KB (101090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eddfdb6cf6edf5427280693935f2555124f345682bd6b851156f12b4f054d0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633acbad1299affbd1576a6fcfbdc46f1ffc81c11bf02b1bc75d4427c2232d17`

```dockerfile
```

-	Layers:
	-	`sha256:91ec6f7f2dbce4309be95b5563eddabd323be54db4549319bb9edd6248226fe6`  
		Size: 4.2 MB (4232403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f0527fd20e9bcfdeb921f6242b5306a618168d939e96b2b9bd5fd9dbbcc53f0`  
		Last Modified: Wed, 25 Dec 2024 02:19:02 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:85c1e998fe5096842521a5b58c6db5bcc89e7a2143c7d9fd4a48d1bcc7e9488f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66279313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7915518302facd8fcdbabaf0e837e3cc9ca822d9f52f05bad88f17932a7a96d8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285a2d916d50108e0806e4d5b0cfee8fada6dbc0363b5f1f194a14b7250ea7d0`  
		Last Modified: Tue, 24 Dec 2024 22:25:15 GMT  
		Size: 11.5 MB (11500257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc896858da3c833c56d11c5fc28a8ab13f16b6fbe38862cbaa105670f9f63305`  
		Last Modified: Tue, 24 Dec 2024 22:25:14 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bb193da8982808546aa6f34961b552e984efee3ed9a4bae2a514be5dc6ac1a`  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e0cb76cc33b913ee236ef79eb2b82a795453b7840e74667b45324a4dee464f`  
		Size: 101.1 KB (101055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:48f993f0be8da4230c6cc95f1e5dc0060eefa4c79cba146ef70974d40cc8f43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f293854b380d56cda0eb4c4425f0788c52b408c220c15090577a85fefaf21174`

```dockerfile
```

-	Layers:
	-	`sha256:e480b7efbd639c10cf37b04f734fc7f41bf6d612d80b033ffa968c48e35cda95`  
		Last Modified: Tue, 24 Dec 2024 22:25:15 GMT  
		Size: 4.2 MB (4229258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0c570a261fcde2126329a286e95b5e6bebb8886fc6bc29652df5e839eb06ed`  
		Last Modified: Tue, 24 Dec 2024 22:25:15 GMT  
		Size: 13.7 KB (13663 bytes)  
		MIME: application/vnd.in-toto+json
