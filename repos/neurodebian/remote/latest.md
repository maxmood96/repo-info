## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:00011d6abd9dde0c59b3353738af9d33eccf7cc4ea75d56cdb5f4b7c0a7d85d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:472f1329af991e1e685a0c932048c2d14a8c70d98212bfb2b0a0ecfea20d7809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14e6cdc54dd7040883ede4dd9a98f978fecd7a3742cbe25ad36c853b168a055`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c11fcffe851b5e799a87d40b72001861eb28a55703bfd725f426c3ece51c77`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 11.3 MB (11266789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7f51c087fd27487523c3326871684de41b31a149a14770bf8119560643c6e`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d047d0a8b4395623517336d1eb42449947af65fc5199dcce0fdf50054d793057`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e6abf1a25573145adc50f804864b0d1ecb2c0651aba756443d4d373fda34b`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 93.1 KB (93144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1166e3539e20c2be219eb033fe86f2ddb2c84eda1d3c7aa003be92fd5abce80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58db5cdd34fafbe656ac5c3dfa2429a94197fa24e2d80cc4c2bb71ede7c76a3`

```dockerfile
```

-	Layers:
	-	`sha256:915f97f64acf136652ba4172c415e4d7c9cd66666c73cf447f8bf648c2ed9ac8`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 3.9 MB (3934172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2642b8e300eca497d8a4ae0d709392a6f61a9fc9533c478d43a7566f0db19163`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:444cd101a14485d17efe5e34036b59e1e7655915ec5567f414d5c4ed7d71c154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836780c2337cb4e0aa9d0b3a5a49f155c4bd7092a81af09317adfbdef7838f69`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e779c0c5fdbd8639cbb065648917ee4734d2cb9fb9c196dba52c90d4da7432ef`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 11.2 MB (11232632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151d4e03d0d99ffb7b30916bb2e40ac5049633d3f098d072e599571fb7187f1d`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797d29db1aaad9bd5c0aebb832287e073ba8dfbf27fba3ce85b417d757130eb`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eaf5a9db5e5b0c8ee5099db68b3227a57c29b9b3bd879c87e60b84a5ded7f1`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74768f33db9b975bfdf336b272ec1c996a074f611773b7c037e26b1c27c55169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efa5d6bf20faa11b566042e290a899de6c2205955a43f9e514ed2898e73e02f`

```dockerfile
```

-	Layers:
	-	`sha256:5f37514115ebad86e05d6e6c9df25bad70e4fa008e3511e2c86d2f46d5ba83f5`  
		Last Modified: Tue, 29 Apr 2025 20:18:34 GMT  
		Size: 3.9 MB (3934426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd890deb3dd68dc857b1766594e01192ba12852af876c01b11f0f3c58ebfe668`  
		Last Modified: Tue, 29 Apr 2025 20:18:33 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:60d143b8d0798ab387a1ba35ab247442d9c6fa2b843bda309178c14872e8d3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff33a1b034af2dc30dc3e9b22bbfff4caf8eaca37fdd763d7e3782238bd6c9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b0ad1c296260622f338606fa8f84c1154fea119b5af30cbf7d53061931020`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 11.7 MB (11689003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfa4f0764baa8548d16c8fa12a59a1e739021678eef8a25ad09b365c098c202`  
		Last Modified: Mon, 28 Apr 2025 21:54:45 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46418c781371c4d88a5c425804320b04a22ddf1058e46636a2ca953fe8730a19`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9675e565699b56bd5cde2c3c03bd8c454537c6ab6beeecb53e9f8a28470b720`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 93.2 KB (93188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:281c23b38ae433c291d7b75e19bb449ba0e2d2beecacd4be15404fae5c96dd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5c9ce8044eee941f00a14266fbd7a0bfa0e4de3155c392b537bb4814d0a4a7`

```dockerfile
```

-	Layers:
	-	`sha256:2c4b6823608fb15cb6808d5a20c6983dcd88cde64abad7c123787ed1955db7e8`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 3.9 MB (3932089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17e7dd67872341c783255b0ba32f6b5c1fcfcdf7fc6cb292b41f934fdcac0924`  
		Last Modified: Mon, 28 Apr 2025 21:54:46 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json
