## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:5abb9c8af6417ceb6a6bd3215130b9bfe8b53aefcdcafe21fa3c89c2f9a912e3
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
$ docker pull neurodebian@sha256:774f937a033e82ec79ed5efdc524cc60f359b1b4578f1fe4f7a90b3a4b378ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3025f51a5e1acbf6054583346525cafa3bd7ca82cd43160ebb36811e1daa5171`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3666961b6d8a250dea41e73593bb3b314425613763ef952df72a2210e3c9db4e`  
		Last Modified: Wed, 22 Apr 2026 01:44:14 GMT  
		Size: 11.3 MB (11273365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6cdd6bbdfee34d91d0fd4ea0fa6b4706aa25b44d362635dd3e91dfb9770821`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e195f58e61236402a05c20b3ca9a451789af8cfb3e1c12867b223461107e745`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33104a23ec2785413870f721ee969d98f2eba62377bfd3becfb8b9c049d52061`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 93.4 KB (93403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56e34690ed311f09247f5dbc2483f0257259f2ca934b4aba64ca6a1ca19957d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda936e5d2e3d4600ddbea0f9c91de89ad2d94e7b306e7e9ea16f25c5a79350`

```dockerfile
```

-	Layers:
	-	`sha256:52a2c953c3a0537c47a81aa029093121fe18618db5cea6819dca6816208ab171`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e210200a09eaeed334b94d7f6f33309c0879fad0c85624f972f547671479418d`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:365aa70bf498507787226c0d7383899d14db803ab0479cbec5dbc5c437049343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fadee2b2da5a6b02cd5d771d3c878b932b1dd725b747cee3d373dcf02b04cfc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:46:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8e0c4933455fc6e8436ccd1a3948e1690ff31ee75a4c911e36f195c9e8ba5`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 11.3 MB (11252926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96ccf4228f5ededbca88454df53e0a2102eaf263c1b2794174d6967279692ac`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334f3723ee4775a37b78eb03aa81e5997c3c1e0db8d9d64523a3babf5325980`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e236fb00fbfc3fa19ecca63a96047f5a436ab74240aa466a134a6de56e34f7`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 93.6 KB (93553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c1f9b95d357e099089706379fe9045341634f3133a97550f62641ab5d1aa96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f564316b6416d5d9f5dd0db415fc439cc4879223077fb341bfcb0808ad3b201b`

```dockerfile
```

-	Layers:
	-	`sha256:f3deeaa1aae3fbcda8209dc59d5ec673ec7afe15fe63313fbed4af3b95c50871`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0dfe5345e8d635cac1bfdec83428fbb591c72ba7827803b3fed0136575d8ed`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:e532fdc0ea71bf3f57b75c5dfe3e485c8fa683ce37f2018faa81b39135dcf09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbdde2c1bc6577d910321443f2efa7d82b6cd57fb77f4825d5384259b8b2fa3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:47:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:47:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:47:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21b39e54470e16d01e012399aef189f5f5d74ebaed5bada0fc42553daf4b848`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 11.7 MB (11692998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e6dbf224b1474afa00888e9da80748007d48bbf2359dfb1402a87a7eda2eb9`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523b5a3359f1839e3db9db3fe09da8f4b97e995fecb115ac4b4b4377c8f27d58`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c86ee33a08dcae770b8bdce200f22862251f08671ea44e074f6f0542c35e814`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a3886fb56a781dabfc8f50ab7d077ccd5dc23b08a8656eb4fed7d721dfdf813d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c6c9429ca0fd3e4700f7bede4fffe9e3b2156597427a811d07466594aa3958`

```dockerfile
```

-	Layers:
	-	`sha256:8dfd9740667879fc3269b51afa30c697791c1271a42bc8ae576d551b790f0542`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f4aaa8c0703dc6cfb4490053062e81b9c1a9b5a7c04117d5c22180eca188c66`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json
