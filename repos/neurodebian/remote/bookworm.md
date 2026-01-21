## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:50378acdd71781752e7024676a8bd328382efcfdfd93b6b5c6a62ee4121d9b38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:07b453c92cf64ff48e660dd4618cdb5d70b3731bacb8d66e1d8c82c3118846f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59850574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2175dda30d850351a8e7c6dcc6a7e321f1f1a792e0a9984968fdf5f6bc26d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:30:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:30:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:30:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:30:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e627397f0fd5d6ba6dc03a13cdb205b2250c665910adbb60908d94813855ed5`  
		Last Modified: Tue, 13 Jan 2026 02:31:10 GMT  
		Size: 11.3 MB (11273362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f47af5f478c211e4a8db978b66053d892e42844fbc976ff37bf72419cc3d75e`  
		Last Modified: Tue, 13 Jan 2026 02:31:09 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211023c1e941ddaa629f23af6b7c6096fa82f8009a3cb6d29440097cbbd881dd`  
		Last Modified: Tue, 13 Jan 2026 02:31:09 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316013a6629ad2d6b021e7d8b44572a86dba4a10a499a15c30e5364945a35d74`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
		Size: 93.4 KB (93419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a76145fec1c345e159dd624403d49f620294a155772313dda1e70ee8720c1301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd924562edf0dbe314e41f14c3e17d3c90eced47af97d807df05d0a2841f5499`

```dockerfile
```

-	Layers:
	-	`sha256:2a89848c7cf3c7209079b048fadd0ea9311760fe46f7743c17c7a288e7e1b34b`  
		Last Modified: Tue, 13 Jan 2026 05:07:40 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df5bc6e443be9b2df1e1fbb9dd364ae7ece7e2a5d4f06ba9325617ba7c049c6`  
		Last Modified: Tue, 13 Jan 2026 02:31:02 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f4d165b202ae7cf889cebfb2f8890f5a1b1e3ac7383ce00db73956bb2a57ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59714711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b050b86537ad67bb9a59f72c77683b3c499dee86aa68bec598ef623163fb7d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:34:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:34:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:34:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:34:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5bac5984f021a1cb1ca749e027c45de7e53293b1625c4988634a4daa8acc9c`  
		Last Modified: Tue, 13 Jan 2026 02:34:51 GMT  
		Size: 11.3 MB (11252918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dc8f152c1cf266e173daf7a4a919546ee4a9897b2895bb2832bd1f63404ebc`  
		Last Modified: Tue, 13 Jan 2026 02:34:50 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c75f7dce09f41ce9bb54cfdcf8fc08fcd6a07d50774a65eb285da7fcd95322`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3504a75e5c40c7856f2d2967e8709ddc3ace746bdc156afbbf077d0ccf63396d`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 93.5 KB (93548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50d1b24cd28126b28a8bc7059cc7aec5bbb328f9577aa0b3467612494ddfe8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b50357eebb778298a3ccd6d4d853257b9c8d1b9e1706a66cd4955ff44f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:a9db612e110a8920702e1d47ac0556074c76c777a5a4f34c6e716b2c48187888`  
		Last Modified: Tue, 13 Jan 2026 02:34:43 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b441564c50d329324650274898a7074bd1b3099aab493b5dc71971a097f1d21`  
		Last Modified: Tue, 13 Jan 2026 05:07:53 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:67812d5d9ba451d131e6983c080b6648e35510efaca0de5b1f1048058abad6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61257184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab86506df32c3e9caffe0560f3b197a28c2c7c8fbd0e56495b0ad5ffa07be1ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:08:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:08:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:42:07 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a556fc2754d9f044d1662e4d79eac9e4915ce45406c40cf4e34e0b2b98dd0626`  
		Last Modified: Tue, 13 Jan 2026 02:09:10 GMT  
		Size: 11.7 MB (11693011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9cb7a9c880a28c145c0be772f574008d4916e91293035f33747c3ddb4f2d68`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167d0a94399112121b938a46fdcecfced399b318f44230eee634ec27d131632e`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331905edb01f14a56fae50e349444847e3bec8fb9dad97125063c168acdf007`  
		Last Modified: Tue, 13 Jan 2026 02:09:01 GMT  
		Size: 93.4 KB (93404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e572b62f187127281c4838b3299293489b0a40b901a9a475fc139531f066fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a320d9dff56836018043dfef369561d75d7d2e35a73b7d9b938c8019818bad6`

```dockerfile
```

-	Layers:
	-	`sha256:712c971f0cd3f560638800376e5c3dfd18579579a9bf58f9575cc4581e212b34`  
		Last Modified: Tue, 13 Jan 2026 05:07:58 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d499e215431beed2308372294ba048f2ef1a48797946500f2ced622d31e60cf9`  
		Last Modified: Tue, 13 Jan 2026 05:07:59 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json
