<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:forky`](#neurodebianforky)
-	[`neurodebian:forky-non-free`](#neurodebianforky-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd130`](#neurodebiannd130)
-	[`neurodebian:nd130-non-free`](#neurodebiannd130-non-free)
-	[`neurodebian:nd140`](#neurodebiannd140)
-	[`neurodebian:nd140-non-free`](#neurodebiannd140-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:ec5c927893e165e413574d4a95fc4aa2bf7daba09f19fc02b9fbae228ddb6cf5
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
$ docker pull neurodebian@sha256:69374892c0ce5a3d9bd103e3b997358c0aa2fb60e06ac8ba2ea3e09bd2b4173f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6787144db69cce1ac94fa4a46bd1cc3735e7e578a4e8704f371e8cca3de11573`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:00:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:00:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecf7ef34f03fc32538b4c6bc3cbf0d01fa667e366f696a2b1b39da8d1d24e95`  
		Last Modified: Tue, 07 Apr 2026 02:01:05 GMT  
		Size: 11.3 MB (11273447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3077df9530666ce829113eb4a39b277d3532c38c6ebb03cfac2a8e95b9cf2cbf`  
		Last Modified: Tue, 07 Apr 2026 02:01:04 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff477a3858b3b073172eb6cbef5c603c6d179fe5c11627c8f92a47ad40df0811`  
		Last Modified: Tue, 07 Apr 2026 02:01:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c5f9e5e22a6c3d7d5ae1831ace77cfc614002176122ba52c76ee3cf1016961`  
		Last Modified: Tue, 07 Apr 2026 02:01:06 GMT  
		Size: 93.4 KB (93395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc14871e80f180acfc726df0095a7322b87ec9ec7c779fdaf5f3902932603a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc52beb3f71dae7afe1a716b1630bee54e197fe4dba13536121e8354084415f`

```dockerfile
```

-	Layers:
	-	`sha256:8edcebcd31c853812834c2af90d7eec07181b1978340cce161bb3caf015945c5`  
		Last Modified: Tue, 07 Apr 2026 02:01:05 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff8fc817494ea4dfad37dd4cb06b2500633f45982649e5054956e53ce4ecd5d`  
		Last Modified: Tue, 07 Apr 2026 02:01:04 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0062560357e6454cca95c4ef20bf2d849b4b3004ff2f7f86bd3f34dd367ff649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0741da89d0cc52e9e35b8a254719a22afcd3e32d5d4591d1e20335186b1a1a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:03:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d1166f044c61640bd82a6fe129d067e7bce23a8dfe007f35bbd3cd6835740e`  
		Last Modified: Tue, 07 Apr 2026 02:04:11 GMT  
		Size: 11.3 MB (11252912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e716b1fa9d2b80c2928865aabcc140f526f471aab2f997e8a02f3968b341239a`  
		Last Modified: Tue, 07 Apr 2026 02:04:10 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402db94ec99e82a9c755850f6f8134a49feb6c9b54dbbdfb03003a9750a712ec`  
		Last Modified: Tue, 07 Apr 2026 02:04:10 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d4ecefa8e2af0fab878d2bb0f4204f37ba290d04d091ccc77fa2387b78658a`  
		Last Modified: Tue, 07 Apr 2026 02:04:10 GMT  
		Size: 93.5 KB (93544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:51978cfc1bdf132867c56497500ec712cc7cfc9fad94fa735554fdf54a88f33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6c0433ea5908d5ff244917a6425460481d58268b3e6eb66f40ed6262276187`

```dockerfile
```

-	Layers:
	-	`sha256:46ca8fbb24a5f8ca822a6a144b7c6f2e1de91320d491c709392af4eca43e1e1e`  
		Last Modified: Tue, 07 Apr 2026 02:04:11 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf45543149a841c10e3f75a54fecfe50d9b9cfd4c8a8952d103d09321a1f3cb1`  
		Last Modified: Tue, 07 Apr 2026 02:04:10 GMT  
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

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:eec5743071ab61aa2cf34da2f1e8a57197d04422ee5dc71aafaf4a519125fe0d
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
$ docker pull neurodebian@sha256:af9f36583560add0684ae7dab1bdb816f61d3f044bc5d455d931f4ed617ad22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bdccdb9cea6c7c13ede7ea3a3b75fb283da72406aafbfbb73813d7525d7eb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:01:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087844227ed0cec1ba8c0d55d16a177a3d958608ac6f329ff2f6c631784c3e92`  
		Last Modified: Tue, 07 Apr 2026 02:01:15 GMT  
		Size: 11.3 MB (11273380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f71f3b70db64197307fb8014659f0717258a59dd1cf269b297abbf9369a15`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9dbdb0f05f5cc24a2a509c37a8a55370a45ec69644733fa4eccbd4c755aa99`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ba3fe3df2cd610b2d6f5af43b9f3aac6f36634eea0c736cb6aa176082b004`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 93.4 KB (93372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed21624c95a06c5fd4414bb36c295eae9a954252902d38e2dcdff94cfa1b39a`  
		Last Modified: Tue, 07 Apr 2026 02:01:14 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ac3718cdf216ba5cd7faf127d896fa8317033f3fc6ecd9014408fe6180c605b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8abef2d402a5dae0cb6e2146b2e6bf0521b504d9d1e81d98e3519375037667`

```dockerfile
```

-	Layers:
	-	`sha256:78653761a1692a80ecf22c84ca7bd515ca9da4cf3c2d746a8da1750bdff35872`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9755936729109275be75495c721adc327e6540f8f6bd7bb7b9da1731cfd520`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 16.0 KB (15991 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:05ae6caad883291c05cf64301ea240dfb58e9ccf487c04dbf125593179065486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578adc7f11a9e18c0f6c3228e563ad98f58d374b38b4e7e76654e19262b20ba8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:04:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f29ec73e1886510fb1ecfb768935d56a0bdb2f3329b6deaed948e148f6e68`  
		Last Modified: Tue, 07 Apr 2026 02:04:17 GMT  
		Size: 11.3 MB (11252932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73e9830f6c7909f269def0fa09293e5734e8331bf6f21d021aad1d19281930c`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d3bab704f4df2485dc0b8b1b1d11c105ada61e1fd0e6720c102bc1bdc764e`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e3f5f6b18c765c6fc844131a5bebbef69e1f6e26669c44008a1ad65654263`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 93.6 KB (93574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19aaa0d12a3f380cf5dac0e4a3d81d3d55b275b9bcb5768f64d5204af903c03b`  
		Last Modified: Tue, 07 Apr 2026 02:04:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a47a902ef9ae281f356a699f0831cba6bb9248423abbd2b4e7fe6a8620bc720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68838707a3e479a7f2dde37704699cf4149b940ee08843fd666ccd5a39314951`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4f56172d14829f8e80f3225a5350ba9e3e6464cc9b302d06f022d7152dadd`  
		Last Modified: Tue, 07 Apr 2026 02:04:17 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d59339a4f579694ce7b209551f0d3b190faf1b489c5c5ad478ed15dd23159a0`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3c724d4e45ca96bebf9f3fe357c4829339b3157a445848dfe46de5eaaae9c3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c734b7942d0eea2f2a08c52e5decee33af22cec203299e20516fd50b63aeec9d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:48:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9facbaad0d2e9efdf61ecbe5eae48392e462f6157769317a5cd77132fb5b51`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 11.7 MB (11693031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a0e5638a1662e5b018e668beba699060c773c9c9b5033e00982543cde5738c`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414a4c6370804d818b9319fcfa6758e633a7415d496c9365dd0a1f42c514214`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df32f075adbc2243cd6c4ca9bd13113a880f00ca717165e78f34ac340e358b`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 93.4 KB (93398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe93084be076971d6e0edf6f5a7b43f04ecbd6ab6bc01a2f0a3194af7cc09d90`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9e32f6700d0f6d5346a0337cda926a571a48e2592e895b59b79ff9c772ad4934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1be16b2bf72dd8ba11a539af912bd560396aa55dae968808a92678c26e3467`

```dockerfile
```

-	Layers:
	-	`sha256:b6600f485447398b6186abad6be1aa3acad2eb1130b9c7fdc1f47432182bf884`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931719e6ab5e367efad0d917c166131e4686443e17a79f01f0b9072b373d387b`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:a58db9b916da0148656d777536016f048df7f1b6a28405090b18d78c43d44e49
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
$ docker pull neurodebian@sha256:815a283965a2981ecf6ee51a3762dade056f8b6a915acbc5e3f5469138a3ecdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64969834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8d8b55687f8c85fd7e2689a535d6d72012acaa28e6fe6d9602fed00b5a59e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:00:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:00:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:00:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8065022d059ed392d247ee0124b58bb237539bfdc595d34200ea8c97c0c575b2`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 11.1 MB (11103504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab6a07c475864417411d527d00df0d98b0f557b781406d9361c50f3143c5ce5`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045396ca6b998813c35ee4c1c1ccbd20c22d6ce39fa5caefc9fb8f9331846737`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc56f4bc3db44ae7b347afafd7771720116653876c5f8247f8056825a18f090`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 101.4 KB (101381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14642158c1b9b01e550fe30794d193bdc595f09fdb031183ca235a566e7a17f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552860e3ae8745e06114c6af91951f12e1112db97bcf42677f1ee66d21dfc3af`

```dockerfile
```

-	Layers:
	-	`sha256:27df89143cd47d37354a1d2b0eed63a352361b45d5372a093e1f7442fe6a8640`  
		Last Modified: Tue, 07 Apr 2026 02:00:59 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6bab210187b27c8fcf0fc2bec53d3e3c5fa6fad583621ded2022c6516792094`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7b4ceff8052908bfbb14872a567901a3fcccc727e78bfcdf19d1d5ccd6a64b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63460822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13047dd3727365a59a6b0d621e288853072e2cbe8f281222ebe1fe7e0e7375a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:03:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0048ee54d91fd366a4e931f3137ac2b126af1e7b08ebb07231f664af99721950`  
		Last Modified: Tue, 07 Apr 2026 02:03:44 GMT  
		Size: 11.1 MB (11109776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b5a53a9448aaac186a68f1eed301f8de1036282201121036969ae74565cf29`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44150457560272e504d1ebdd644829bbf7c9fc822a6e923351e83411352658de`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46546c3a2c928c07581b1783bb843e469cd284b449d83d28046f1d30069230f6`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 101.3 KB (101272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:07bd9797a2b35d146799913fb600a653b853519fd4159f0677fc9c18253001e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7bc4db97feb07af4a4032212394e233f57bbac16e853195535454d41a9a28a`

```dockerfile
```

-	Layers:
	-	`sha256:53a269b9ca5986ef3ebbc1971ca4f6877b4e2fb72083c3d5de4f7dcdf794ae12`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a240a1e68f3965e2ff7da060a77725465f02cd8041baca3738f6b0dee08d254`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:17793f7beceb2301200093eaa872899b8f20ead35b93dbedfd981183f89f29fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6cbef88dc1871fd829472d420d8aa6a5b9e2025757991eb9a1fb169244756c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:16:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:16:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:16:13 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:16:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f876b1db5bb9c9255bea19ae18fde9747fdb0c02be464e9379fa51c73d2f5f`  
		Last Modified: Tue, 07 Apr 2026 02:16:24 GMT  
		Size: 11.5 MB (11502348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5368ac9a74843c95e70f77bbacac35d2162ffd6aacf13ada3d871c8775775d8`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d920dbb8d782826431dc24219d719874db195b5c3204623b900bed68910d5`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f782acd2f323b11fe0ded7a1fcb099c41b8d25183157922c41891127243c5875`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 101.3 KB (101265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:18247538bfd3db99a32a3758e7d03994c39a2e2ef1595d508fa2dba7ac77fb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302c2b4c9cf24812a3a1862a60bc8b7b80e60f7881845d9fc04d388753327acb`

```dockerfile
```

-	Layers:
	-	`sha256:e04f46240354956e7214563f94cd809be7295aa5e1d169c9b958b714fec79ab8`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fb8255945b9e668090fa3ec96598e2849651c55338c00303b5b49d1bbeedd94`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:86178481890d97f684454ded53c7f45765f092bbc50ff8ce6499015d9ca48ab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fe085c2b66f5b98b8dabff665c090189b22b35705127c028d99a9de4ea2fbd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d884fcd0aa0fc7742ce71fda5592ddb3bdaa70abcfec2639be95de666e9a24`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:00:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:00:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3652b2041f6d71d5a4d2d4ce03be98853d697f2f28e3747ad8472df52258c718`  
		Last Modified: Tue, 07 Apr 2026 02:01:11 GMT  
		Size: 11.1 MB (11103609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072842f241cf41b2f78c655669448e3045739cc128d4db6f0e65a677f45acd35`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d227b73727a72f1240902141a5dd294aa2e87c47192b9198ef9072bb1e18a745`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d69b4dbfc56c2df58387113855e5cda409a9cbfe3d9e3ce402f3b5df010a35`  
		Last Modified: Tue, 07 Apr 2026 02:01:12 GMT  
		Size: 101.4 KB (101397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d923103343bc5dc334553f01396291d7a8d9d308763f616c40e0ebad605522`  
		Last Modified: Tue, 07 Apr 2026 02:01:12 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5b76ba35ffbf45b3b557b0eb3b42c7cc0a670ebe7b740ff28abc6f767b68d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5908ada024d71ceb6322e907e608c6a0c1ef4c4a62b8572c340c9b61e67b460c`

```dockerfile
```

-	Layers:
	-	`sha256:5b60da26860f07f069517505df7fde872e2c1542956d21035e652d9f1d5511f3`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a009cd19fa2fbddcb46841f1749649b56cda9c9f4f9b995b420d772a73b5d7`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8ebafb70a46289d45705b2924366ac85b68c040fc9b4fb0d212b6e1b14f3e47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dcf58c6c976daca65f1d05ca1cbe23a599a739b69de86a428b1cd743704180`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:03:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:53 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83dc7b608ee9f4bda69e556dfafd08b0deb8c7d5b42fa6c452c69fac9069b8f`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 11.1 MB (11109902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb66da7ba94831ac5b43b51d0a0aaf36b8246252e087373ab93e36d45e127d37`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901116b9c6b476b402eba10437d139accc48117e8396221afb2538026b321972`  
		Last Modified: Tue, 07 Apr 2026 02:04:03 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02b336969d84a4c8e10611b9c2470e6dbfdae6cfae1ef73b5745974d357c35`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 101.3 KB (101300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e190faa9f5e8d05e12f9dbe8984c181f00be94a7d7cfd8b8d4ca3d0c972c97d`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f59235285ee52e1f4c43c5ac7bc42631e373265d406e3a2a873b4ecbc791815d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3628bf8275b73b66b6703f4b0a233507b559112334b32eec23b58647aba7a5cf`

```dockerfile
```

-	Layers:
	-	`sha256:a7ede3816ed841103388f14a094f99b57b7988e98aafe1c9b20aa2ba51ea19e0`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e813811093f9223245e90f6a2c4e5d36513fe28f4694e3d10fca9fe6b70c9887`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7579a35afe8e174ec62d633c68614ae8124f1f401a290b9e69c0f62d50a5ef10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66308720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d676756c0d27d5b94529bd4c6cf71c8d72096117fc03c9b367501f8bbc5f3d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:47:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:47:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:47:57 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fba7877b3ec8a566d97b730194c65658357ad675cdff2c35c6c1c8b5deccdb`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 11.5 MB (11502302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850a009dd4f23e9a62f33ec76651cd49ec853a8fd4707631e6d659cbd4a056e9`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3ba9c78991f613b0caa3f2f7156d2cb6faf06ac0d6819d4e02644dd1381e0`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b6b6dfeec66a8cc3a24e834879c3b4d6c1a36922d9d638bd2db930dd40044`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59daf1c381bebf5c5efa361f8527b353c71c67fe360ebb066dff44e164e82ab6`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7c5a566c3f8389fb009e31a33132c70c124e29e40a1eaf7c7d2ff15ddfdb3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440cf12cf83a85140c6cf0ea5e40617e7189077c445023cca2e79d2844fa2737`

```dockerfile
```

-	Layers:
	-	`sha256:3f915c61028bc950f81318a5b1cd11ef596cd314b75ae7ac01ab9084e21f0ca1`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79910c58c46c2b4404c3dde156e9cd6932bbac7116f4d759f11d002c3b02bcb`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:6a9017b3233ca41ed67797e5fa2a865ec242517389843412a4421c57abad4792
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:9a56929fedae0662326117d6e5dd1e0b2b7cc1349b2cf152a987419e3182fb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60059477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a609d06b9d7f0b4722b4c0037179341c8d091db52c33cf1103a260e0a9b43a3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:01:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a619bb3c1f14c591cc163d929ea3f43df5d6acebdd877fecaacf054d56531b3e`  
		Last Modified: Tue, 07 Apr 2026 00:11:23 GMT  
		Size: 48.6 MB (48587084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d037c825c0e23aeadb006f5dafd902c14d32ef6b778abdb287f93ec185f4afa`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 11.4 MB (11380112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17caa6cf3bd376e27df6ae0c80cf1e1c499cce5c07af7b0f4c9a4b5c99649a0`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce0cd7dafe8e8815c85d2c163d5ee73efaea39c8aa25dfd85fcf04a68c46fb0`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5997db4eaf4518112a9a1ef15b02a9a3ef54aba63befeb30c880c36df3dd9`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 89.4 KB (89377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b7d30b0064f7f6542b44eac4be7c4ff5472243a82a54d0e15439ff1ac405c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a159fa7cae1094bd789db22a82737f1598da8ff91aa7b6a2eedae2ce25757fbe`

```dockerfile
```

-	Layers:
	-	`sha256:08e0eaf65642634d33d2de4b38ef140e63c924edb46b26450537d51af1f384a3`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 3.6 MB (3552027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac83dec5d489a6bbbfb99b613e3b54c0ab6be04c9f9670d0dd7605524640fad`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edb2b53157537c2d2c02dfd8eece602261263f34335795b69eeb92d36f5af494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783523f0adabf2862579080f534b06b40e27599b5393c28a50d158d791522d5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8be2228c7df976aa0c1c2333d6e8d72b206ff7533d4625ffeae3663f7240d98e`  
		Last Modified: Tue, 07 Apr 2026 00:11:06 GMT  
		Size: 48.6 MB (48643356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697160fe466de149ab190bec6e9e1290ade0a79286096e7daa5c760e60197f5`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 11.1 MB (11075013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c36960bff1a2ead8dcab909b24198e7190f9e0116e4fe6e295d76f8078a6b8a`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c1b95f12a1663dc10a0cc935bb1a7e9a7c5991e3e62be7a88b1d82aa3beb00`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a92fcb7587a72995d5472a8ae08413c3262707d6d83ee78a4498382240cca9c`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 90.0 KB (89989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:df205eb13b6222d0b2746f3723e697c01e488e9b92727d7dea12dd97cf3656be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94c537e2f013c3777b8e6ed31123c1a89e866c06cb72480cbd9307cc2cb86a8`

```dockerfile
```

-	Layers:
	-	`sha256:65718c326ca36ce31873d1b5c78aa7554ad5f5bb91e9c8c5367648577e6deec4`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3558012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18963cf37800d3076a9518339af99dd3f02829ab9bc2067ecfe637935cb8616c`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:963e9e111e8de94cf6f0bc0fd6677f10f9d66bfcaa1ab43ea137bbbe888beb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61577258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d79aed3d5d0abe958e1d97fb8c77b27f9058782244428ed88556d34491bd44`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:48:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da53d68ed4a6c93e46a747a177c1be57f4bedc8509f9b442a53b6120f33a247`  
		Last Modified: Tue, 07 Apr 2026 01:48:55 GMT  
		Size: 11.6 MB (11606305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274d6db09e5125c5a1f35e35a167fb6e882923e24a15fdccfd52ae3c59f13988`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e4cdfef32a160c154e91fc59967a8b5ac1c481c4b43b670dd60dc11820f3c1`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9110c7b8d6c12b2a6cd0a52f39f4a960d1d3d9252246c30e1fa606d606b5d24a`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 89.7 KB (89656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f1b6fb33d3cc7c53d4c45383340dff8aa68b2541fafda6f159f57ee8a6edfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f3004b499770aae74ad966f0b5757ca7e53a5920485fa3968c47aebdb71fef`

```dockerfile
```

-	Layers:
	-	`sha256:2a79d047e2b4515eda42e50df12461392fed49171ad04a9ce1f1d75ae60fb003`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 3.5 MB (3549980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3bdd8d104ffc8e688a0c4a90fd13b9f18bcd3cfee4cf483f0a2a5a3114b82e`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:eacfbf31285a85424ef93cc6ded82ba2fbe5b986a239fd69488c80f0f710945f
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
$ docker pull neurodebian@sha256:6a2235613045b70910bef31f95d400e4ea728d3d872c3eadf068ad6a5556e46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60059992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc43089ed9146b80ec6df0e482f668dacfa87f89c583de65af75120f18cf742`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:01:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a619bb3c1f14c591cc163d929ea3f43df5d6acebdd877fecaacf054d56531b3e`  
		Last Modified: Tue, 07 Apr 2026 00:11:23 GMT  
		Size: 48.6 MB (48587084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa628479b442faba1c1af937394fb683eb51cbbb599e6c4a61d0da961f2d7b3`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 11.4 MB (11380125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcd0304f3bf7b2e1d0efa613975496c67119b2c9e846c5e0c82ebd89a33967e`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce0cd7dafe8e8815c85d2c163d5ee73efaea39c8aa25dfd85fcf04a68c46fb0`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561ffd779e9b744ab3a7ec489f3193657675d1cc63c19bd41a103f810ae0d39`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 89.4 KB (89428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162049e1938cb0cd398aa0c3337a92e241d35b71469a0f3b4afdc6d8facf563`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ed69fb70e1162ba1fcf7caf8b043e147b224c0d768ac9281501a7da25ba4095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5525b32edfe7cca39b6fdd26484b40000d68927bd7d2b0d0a97afa4ef4c6ee3e`

```dockerfile
```

-	Layers:
	-	`sha256:918200918934c6226e2f5e22c79c036415cd438d8dffa4614ab7774fde9c2f2a`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 3.6 MB (3552063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8743c2342684b499a89a50ccc6eac5a1b7ca15b9de0b45b1483221a3422faf17`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ba0014eca13dbdc8c4c9695ee548e42bb17ed8f9a8fec425adbe0fcf9acb7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b39cda1b57a54ebd323ebf1b4371137f41bf6723582d02109b35182b365179b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8be2228c7df976aa0c1c2333d6e8d72b206ff7533d4625ffeae3663f7240d98e`  
		Last Modified: Tue, 07 Apr 2026 00:11:06 GMT  
		Size: 48.6 MB (48643356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b0a86641588b3f119195f4efde642f305d497d115b96e5242a1228f623b53d`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 11.1 MB (11075059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c36960bff1a2ead8dcab909b24198e7190f9e0116e4fe6e295d76f8078a6b8a`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c1b95f12a1663dc10a0cc935bb1a7e9a7c5991e3e62be7a88b1d82aa3beb00`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daedc55759c57539904ad5f302a8d8ac0ba365cada751eb464bce0e48e80211`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 90.0 KB (90012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f8aee6980d05907b17819acc5238181f4a4b97ed15b077d9c94676b52bc1e1`  
		Last Modified: Tue, 07 Apr 2026 02:04:34 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:10828bda83635ab4504a20c3acd44d301d95f70967ba4152cd754792d543519d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc48a161a9fcacbf8106a2b73a2a6a135fbbc570303e482b580cf3e410d897fa`

```dockerfile
```

-	Layers:
	-	`sha256:14e69e855ee2483f98fb85b5ff935450656ad764571383eec285973b6a0ad358`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3558048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcb49532153075f479fa9e706d3028ce305e2d853eba7e7ffabb7342c1fa372`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9bedad4528e45438d1623fafecc7ebd4869eb410b0dbb85e4a82aef61511431f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61577804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6518c25eacd6983972f820d07b0b03542e361c4746f0212991a4ab16af0c24ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad078a61f6e4be70ba6616078c3a30d7878e3c52bb074b890ccf08d7ba6c0c01`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 11.6 MB (11606394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d033c8c40129bbee090a07f5e1df4ee001c1ff1b1fd1e0e8fea876d4dfefe77`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6602b36874f6c218ec4f391df4b2e6eb6c4bfd9979f4f111c5fa69b47496ba2`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d50765ea499d27dee96965b634aa3a32c0fba2532d7f79e39a9119111c42be`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 89.7 KB (89666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedfedf99f96257ae9c575d353d0f5d352b036e3a8c97cf7a608eb3837152eb`  
		Last Modified: Tue, 07 Apr 2026 01:49:01 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4750e3e14c0f736243e2236c09b7da62c1b16042e8849a8a4da7588e6081eca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3479307f59614f39eb4a0fdeda1168462dd3a6ab17a49e6e26b68882d8a5e8fb`

```dockerfile
```

-	Layers:
	-	`sha256:e0ded4254441e42d507739c92b200d27c9f0e81de4f3ddb5ef6bdc0428724d01`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 3.6 MB (3550016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aea253b22bc3a5f64020d8dc3bdb1ea14d6dc3aeae1db43327b6b9d33432be8`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:42a6b56811f661930f4480bc40cbf6e91be055b507c08a3ea9b291429b792e90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:e8903dd5f18cc82e3fb1e884ae1a4746c7738a2847ad86f175eb1b62e70e5d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59724e8c9582356746478c7557741e3e11c464edd6a3e13ee3ab2c3baaeba8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:15:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:15:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b205272ff28d72a83b0c052d9f36b45fadb2a03ffa45596ae8e69ff1977fda`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 3.6 MB (3624564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa7cd09349e4d275f5edb2a27bec22260472d5e3de628b17bcf1264218cafd6`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cfe116cfb8c04dba59ba2510192972d47fca24b0d0b290dc85565c14a7bdf0`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c19e2b3f2b0bfa3e6f4e9f975d5eb097d832a9072d402567e9c26ecfc34a5a`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 111.2 KB (111198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1cfa6f37839f2b9f2fd9efc7f1ab60b9779b0a14e8e7d89d043ae54fa9e4694f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3b7fa07d975a595a59358f4764ec240a8eb7dba0a6cea3228697f3b0843a3d`

```dockerfile
```

-	Layers:
	-	`sha256:714a5735345c61cb4295f36de327f294127309c242243f4166317465165377ae`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f09df083110f0840d2504cde969b323334a83985c62290499a3bf8a26573aa4`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:56de5ce50bc6484dfad202db32b89a2f2ca4d48557aa48e4cf11d390d6da73bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913e7ec62ad9077f24a0b24e72ecc4fa55fc5e7b77ce11f79f53bf152cb8eec1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:14:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:14:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f628ca3d20e1c17214b7d1cfb648c745e7ea7a5fc3188f05a7a757a2de998d`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 3.6 MB (3604788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80793066cb18af083cfac67a17a06c1e4afd12ea6ace3fa8f6f8a613d469756`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368eee4161f30a527478029668d0d63de762edb4a59fba3555fa62c09279eed`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3674a38a9279ec2d8a0bb18ed63f4e177a930c5e9be7229b354701d6769b50`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 111.2 KB (111153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:12e4211b6e6d2c9a0ea2b79782e147901a46b2ee80063c345077a1ec63b5cd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8c580742abfd21791b0d471b0ce3169207288db6a9055b3b11eba03a1a593f`

```dockerfile
```

-	Layers:
	-	`sha256:391329d2b648bdb436cd1b6af1bdfc3a3143bfb69f62a4fb083a16013a6ae01e`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31201397be8aef44a004153ad48cb4a0c7c73f929badb242256dcd2610935155`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:392dbeb6af6b687493f63cbc5e1ac017a996efa42b7087014190bdc9ee28d82f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:94ce1db1af85450c8d68a617194541b3ce4701341bd8f5720a7d56aca43c960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f6a6e5468c8cd593f014c698ec62fa71c88440f0d5d42793091a5572e2cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:15:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:15:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d80b2d6b05311b2bf85ebb53e3a2513e5705d12a9123796d1c6ea60554e651e`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 3.6 MB (3624576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ea02e1d1ed6638f377e1e099a7b43e52ef2b4298495dae050273e351d29265`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf0571466a6f5648b0698f0a4be25f95e6b2505ae70977add87cd1aa6c0733e`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78758f11159b40c258ca47ebcc824379dbf5299f8c350a93ee15d41af341bcb5`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 111.2 KB (111203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58eaec0b4361bb71faec94c13bf7b6ba076efef6e254f966213ffabd6815c3c`  
		Last Modified: Wed, 01 Apr 2026 20:15:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:92075526fcd071ad41feb014f0acc16d0a42dde119562cd26d47d86713bba3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6b55cd81bb43ba395287c451f75717548124cbb1de94496a18b8f0b6cce6c9`

```dockerfile
```

-	Layers:
	-	`sha256:3a39455db87e67b1acb94e008a6bf7932a50406749255cf986e186fdbd987c07`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7733d7a85b8661d6ba394101ea5f0a1cec8218b5e283652cd2fddaa756ec7ac`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:394de8222acd546223af23904aa1ed27bf129b9229cd1870d371c159048d9a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51928ab1653f2d374fa511b1c7850b344a4e33a52a58812c7a8ee6ebf75f6a8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4019784363cefaaa0608f44a7c43404f1b49123f5490bd18ff61d334344dcd03`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 3.6 MB (3604713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac14a880a2f296e4a09554d5f7d84793b55df94e7b4c331567c990b3480470`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7b185bb1d3b8189d1af6df1aeeb5e439b37bb515e3842af0b98424dbe2a5fe`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736213a2d43cf0f24c9174b8fb31963c318bcfb6708f00ace854f394cf5e34f3`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 111.2 KB (111166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57c1c1d3cafd08cbb99d7170a7ed6f9d171ccb1bebae7ca7ed6a66cb514d61`  
		Last Modified: Wed, 01 Apr 2026 20:14:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1c5645de0a996722122f4c9fe0b9ee1feb9f9fa5e235152031b99bd71d3229c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb25718c8f24128797396d2c2b144f786d6ab403adfddb2df3c99adacea0df61`

```dockerfile
```

-	Layers:
	-	`sha256:0957159b9394ba37b209348e8d8a8338cef651a44bbe52536707849659184f84`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8676f87d12d1ed89bca09e6bcafb4093ea3eeaac8b18ba0f5f60591dc4211c78`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:2f4c470979405f043d5816a2dba54ca07331e342b4f9a7db2e47a6c3478f43ab
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
$ docker pull neurodebian@sha256:6c104489228738831d5ca33b6baf71ce5cfc18b9e9f7bc0d14ae6a445dfe0c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3c00b85430bbc08735ae3ead27683573e91bf9af2e8f1dac4561f50996dc0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:01:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491dd2c1ce4a7e4b47bb0f8c8b741e73a78e971f2f0b5f576c0b20ea8c265992`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 10.3 MB (10292926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499acfb1e6832771a0807da2c835d40a0fcf56fa1e829aadeca0574f98e59cf`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3cda9db193172c74664130719db3132d8bbab1895244ff787f388fa27e8be9`  
		Last Modified: Tue, 07 Apr 2026 02:01:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa31249a55d68e978373b17a3a29045fda264a2f48ce4546b00e5c7df843de9e`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 90.4 KB (90419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5013919ccc9ef92983a73ab94bea9b759b6e5d9bc0b349a0c5578a57eb01196d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e767760a21268d05f2acda8a74b7dec0ca65ac8ecab817a8234bb4383d5b57f2`

```dockerfile
```

-	Layers:
	-	`sha256:c537c6e052c78b4e59bd6777ddc6484a9a231f89d686f491afbc066bcf392bca`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f9d0e0748809704210bd279c94b612a1fc365276fff4575ac4651202720d38`  
		Last Modified: Tue, 07 Apr 2026 02:01:20 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:58d1bd7459c21ab1d7a283920ce3c6da18d960096352c0ccf2535b25d1a4250d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8775e554e09da19bca8c4c969d979b5900d0dfc4e5faddca26558b30c893ff2c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:04:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e31d89380ba732a0406195a80e8d1f3739c5ccfd5c102147c23a0a8f4708d7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 10.1 MB (10077988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2483c2d3147352a96a1061695bd50cecf1a77bf57f3a77aac478c02f0f67ef8f`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2751667ba5d31911e37cce1f7dfd23821525fb957928f5faa8a6cdd36d3b61`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420205519c6217769acfb298c60c3c469bdb5371378721822ef809caeae63ca7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 91.0 KB (91038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b30f0489d7276af845415c7260183e991fc4cd8e77740cce7ec7d7e141690b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f8839bd68e19d91358b5a5abd666a7a4e5fbd79c831055c5c36fe6db305ae5`

```dockerfile
```

-	Layers:
	-	`sha256:4ba20350eefa715ad7383f1264c935f46d9475f86c079fa66d4a2a7eb7cb8de7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fbf8fad5f0b3b5169e280dc6798fe61163081b0b66a7b5f3e18062d3ca4f133`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:422c2755b2e1bb2cd368b83e6a6e2c89ab0a54fb5f4848d7e2e4f6a8f220e7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545007a21b6e79e48db521a82a8df542d7e10a15a63e5d34df7a68e6b0e17388`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae1f0fbac6a88be9dcb23c571da82da088cadda19b034b842e84cfcaa28f452`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 10.5 MB (10467068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754115c41d1776cec3df85c51bf394a2902c4eb791f82968f19c476a4eb2c6ff`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f12721908b18e9c6e9b6ceae633014052eeaecf3932e098fd33b5c039692a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0d1e672a9c3716d3995031e1bccf1c7cdfc458eae2a4dc4586cdafed0da19`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 90.7 KB (90742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ca41842e4de756490c8d6ea1114951e8a19bb5e3d1a854c8a444b58430791eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee0777bbabdcec9770ecc591bd196cf2bf6b83641b2694d4bb341221b144989`

```dockerfile
```

-	Layers:
	-	`sha256:df67e9a01457161fed449645509b7c5c64fcb4132915e5ad855cd6dfe596865a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c16755d7777b7d788fb820ba0fc72234a522326dbec9d099a8f50ae45927358`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:25e9be42321ebefe6ba08a0c5d941df090d2943c03c2af4cbcedf72afdd26120
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:6d1e2474b98c2a1bcce15b241a355af4da64ec06aa918936617898d29512ac25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60171574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac865a5fabef498174fd27d645f2ae8be8b6b6fde69f727b75846321f55cfc7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:01:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b208148f3abde07a5ac47cf579ac1ed4c9312d2ae485addb285765d8008fe12`  
		Last Modified: Tue, 07 Apr 2026 00:11:41 GMT  
		Size: 48.7 MB (48710648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9680cfdd3e4129a60748e1904e29c37d431b0b864e26b6cc1169ffebee2cb75d`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 11.4 MB (11368683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d3bef65c117797166ff5ed760c078a32b15b167e32a553a29c940570822487`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aa0f33df95aecb126fa27d57bb3a070b44e34656956e7fe0264b009211d5c`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d45a5729852586277730461289592c04d0e6dbb72de0e324fbe2aaa4ed9d4b`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 89.3 KB (89340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:963260a04a05bbd3ebd62d35d0e902a265a373f9de3ed9623ecb6cd28dae7f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1362085b857b4acba8f4275e8aac5c6c836e3fe86647fbe51b6e62fa976a2c`

```dockerfile
```

-	Layers:
	-	`sha256:1fe4067892c99e2cf5bc78a6bd50a625130390f8b50c68533758ac6f5af8cde6`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 3.5 MB (3549087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a3533b60c61480c4ae00331be5f79ccbbc42761982e303d6ad716012bf7c297`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:31470d05e1cac0a1fc11d2a656a7e2d8dc2144bf2a61a17deef16a5c76919400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59910208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bde8d257c76a0907a0d9b72dc78d5c7e23faafdcd8a3d208dbc5a33e2bfa443`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ac9c76c00b1b19d9057c64eebc87efd57976d9d3d4373752703081335cbb1900`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 48.7 MB (48744945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17966fa7c8589dcf8dc631f45556cd118e6cfdd3792e0d613548c653c7ba358`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 11.1 MB (11072457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945ff9025edf778838c09cc7ede3fe6e4d78195d9a5d83e9a08d56f48b8a57dc`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5466b442dfef5b49389002c7e3ad8b9c512754b0041f963eb9a349bcd89b8e23`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0177b69925e015ec37347d8c984b1cdac4793c06f8deb29a244711fb3acc3df`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 89.9 KB (89905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:59f0686f262a5e90c82fe3ffcd59f58fdbd4fabde77ccc91b6ca3abec5aa3dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9527f078cabafd1d52505d1cdcd3bc968dc8970d9f7b252090e846771bc23c71`

```dockerfile
```

-	Layers:
	-	`sha256:1b37a51526a10036207dc61b7842830789c3a2421a4eeaf39bd1e53632363669`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 3.6 MB (3555072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0362e5d5c5cf674f3f001c0ae6249f64af6a3f8970763d8d641c0b28c56cccd6`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:c60db7eec078dc52dc2c3c428344e9aa3479b05011d9d5b163e922dcabe8d9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a656ef86060ebfca5428834bdfca9780b93a6289decfe8dd3876b08d4ad85a5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c3a3fef3f09f7a3e83440b35d7d0f2f724470aa7260920183b022678103935`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 11.6 MB (11602235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53125d28144aed0499a184d660c37574f5dc0488d48921247a3954c584682c9`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca2c3c8f62c3c8516fcb39ee0b67f5091ffee2f35935228425aa07bf9763596`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a659b6eeb646760fd0e9d056438b39521d4fbbcfedde6dddfb7eeef1e8767a`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 89.6 KB (89635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5c2f9498331a592ff803623a19243947488e9062f3f57380e234383c343586fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5a868a104e8cfb4ba4bbc83480a466a971b55003ae7fc8a98d712b25c1e30a`

```dockerfile
```

-	Layers:
	-	`sha256:a58c065d6365faaf3bf8884ca4bf9f13bf2e669f9f981055bbf69409b235f0f9`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 3.5 MB (3547042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be546487457e10b6f2e2f752a781790dd2d55b4764632002fc8e7b752c8b4268`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:24e14e1b58a1807440bcda71183138921fe9bde3590d423cbe3440c61a75259a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6a97ce654e0eb6552d2bb76efc3454ead70afe0a3fc2fa654673e187757038ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60172027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a82e705f83fe881c5e5f192d8010788c9bda962a056898feb36bb82f4f4b26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:01:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7b208148f3abde07a5ac47cf579ac1ed4c9312d2ae485addb285765d8008fe12`  
		Last Modified: Tue, 07 Apr 2026 00:11:41 GMT  
		Size: 48.7 MB (48710648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e359a898b31b0e9c8c58f608eaa36be1b8c82ba572cd885ddc5b74e54fa00d6`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 11.4 MB (11368694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd15120090ef6e6a2c1358a10ea832b710c945b4d206662782e92c9eb53a2fa`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aad35ffc48f0873d152bab616af660e071c2abeeb01fa91ce78f73e038f5db7`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7f82a3b3c524294cb678870650f0f1daf178c7144dc185a3d53d63e878ebfa`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 89.4 KB (89363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f0c8526602a286d241f56054e7a00313cbc165ad25f708608ca9977783b8d`  
		Last Modified: Tue, 07 Apr 2026 02:01:45 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b53f533863a2d01b3271f410c55bbe4efb865cbd221fdbe4302e9cdeafd15e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacff77bbcd6b5fcec98b0420bc413e3a4f66b7cd8564c4a2ae88b63cdb57a66`

```dockerfile
```

-	Layers:
	-	`sha256:f57d844cb34d7a636b5e7f9214efc0f0153dc056af5e3dbf29c2f46a067bc9e5`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 3.5 MB (3549123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beb01c446a636d846ec76ef42de8f855540cfe404fa11aaa94e5977b15beae3d`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9c61266570716a76fa4d66983ae408d5eea38ae55812bce1046eaf473ed9b647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59910666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de0c61091b23a1980030577b83f83fabb42b6738b3662f056ef9049f88e3748`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ac9c76c00b1b19d9057c64eebc87efd57976d9d3d4373752703081335cbb1900`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 48.7 MB (48744945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85840404f57afb5787eae44f30186f8ebdedf22f7341260a6d562a2e16e6d27f`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 11.1 MB (11072472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf44374b898e8eaab4fef95f90b0e127e4f6eed7b5bbf963f568241a8fb2e36`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c14cd1ddb0b2f50fea0a090beb46755df524ebce2f44860805c804bada8407`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7c94331ed393d89b3a0b7e290ccb642a59a75c1f15fa8c5bf35faa73cff651`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 89.9 KB (89925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38896d5a61d5211f6261adda86c26527050e97d2538d0838ac55c5cecec9002`  
		Last Modified: Tue, 07 Apr 2026 02:04:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bac54ec2ea8eb1dc276e26335cc80a4a48ef1c43293159e45895ff1de30d0bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b089d25c53dca863e9b1b12b678ab6f783254e946af06e2e5f07ce7f16f001`

```dockerfile
```

-	Layers:
	-	`sha256:25c5712129944c709b840f4168586b4a685e4b2c4688d661d19a9dd73dba8215`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 3.6 MB (3555108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f09c4d225542d79fc824670a13b384c9c0686035eba21c64e7146ddff3ea29`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:379dd6cda62c5f956daa4957282d12057faca8d0d2edb10eb00b63aa4b127649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61688954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4690074633fe4fccb4c59a578a84a38bfc055cd41d859f3fe6750c62c03075b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbde13ff2785b11cd70a92d1da45b61ee2c39ba77f505a32b6764e1bb1f3464c`  
		Last Modified: Tue, 07 Apr 2026 01:48:59 GMT  
		Size: 11.6 MB (11602276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8a43f3df2ec92648d7f9cb6ae9b59596ef7550e9b2c0de212a9d5067d70eda`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8292b280ecf08c2a53b62734b37ab925c0596e7c8837ab862f48b6ed13161a18`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4fd33efcb827f079f283388221dcec47472439dd679e48cc1dd8c9c469c885`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 89.6 KB (89646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee066862e919913f4a8149190cef898dcb0dd51f675a1b0b66cd695eab88dc5`  
		Last Modified: Tue, 07 Apr 2026 01:48:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20806508b55568c0a85953b30cecd0be318bf1353380d952b6c350c1f23b2cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58350dbd42299c78510c7b6d6e14c04f9e9925d1c2ea28148368a9e35ce4182`

```dockerfile
```

-	Layers:
	-	`sha256:07eb593648572153e5a66df88d45281816a4595bd6859d58ff20b91cf3e389b3`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 3.5 MB (3547078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60adcebb1386384577e15e4ca93b84d41693ee7655e05bbf56de36d0fc4ace0`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:a58db9b916da0148656d777536016f048df7f1b6a28405090b18d78c43d44e49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:815a283965a2981ecf6ee51a3762dade056f8b6a915acbc5e3f5469138a3ecdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64969834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8d8b55687f8c85fd7e2689a535d6d72012acaa28e6fe6d9602fed00b5a59e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:00:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:00:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:00:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8065022d059ed392d247ee0124b58bb237539bfdc595d34200ea8c97c0c575b2`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 11.1 MB (11103504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab6a07c475864417411d527d00df0d98b0f557b781406d9361c50f3143c5ce5`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045396ca6b998813c35ee4c1c1ccbd20c22d6ce39fa5caefc9fb8f9331846737`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc56f4bc3db44ae7b347afafd7771720116653876c5f8247f8056825a18f090`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 101.4 KB (101381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14642158c1b9b01e550fe30794d193bdc595f09fdb031183ca235a566e7a17f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552860e3ae8745e06114c6af91951f12e1112db97bcf42677f1ee66d21dfc3af`

```dockerfile
```

-	Layers:
	-	`sha256:27df89143cd47d37354a1d2b0eed63a352361b45d5372a093e1f7442fe6a8640`  
		Last Modified: Tue, 07 Apr 2026 02:00:59 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6bab210187b27c8fcf0fc2bec53d3e3c5fa6fad583621ded2022c6516792094`  
		Last Modified: Tue, 07 Apr 2026 02:00:56 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7b4ceff8052908bfbb14872a567901a3fcccc727e78bfcdf19d1d5ccd6a64b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63460822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13047dd3727365a59a6b0d621e288853072e2cbe8f281222ebe1fe7e0e7375a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:03:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0048ee54d91fd366a4e931f3137ac2b126af1e7b08ebb07231f664af99721950`  
		Last Modified: Tue, 07 Apr 2026 02:03:44 GMT  
		Size: 11.1 MB (11109776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b5a53a9448aaac186a68f1eed301f8de1036282201121036969ae74565cf29`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44150457560272e504d1ebdd644829bbf7c9fc822a6e923351e83411352658de`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46546c3a2c928c07581b1783bb843e469cd284b449d83d28046f1d30069230f6`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 101.3 KB (101272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:07bd9797a2b35d146799913fb600a653b853519fd4159f0677fc9c18253001e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7bc4db97feb07af4a4032212394e233f57bbac16e853195535454d41a9a28a`

```dockerfile
```

-	Layers:
	-	`sha256:53a269b9ca5986ef3ebbc1971ca4f6877b4e2fb72083c3d5de4f7dcdf794ae12`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a240a1e68f3965e2ff7da060a77725465f02cd8041baca3738f6b0dee08d254`  
		Last Modified: Tue, 07 Apr 2026 02:03:43 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:17793f7beceb2301200093eaa872899b8f20ead35b93dbedfd981183f89f29fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6cbef88dc1871fd829472d420d8aa6a5b9e2025757991eb9a1fb169244756c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:16:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:16:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:16:13 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:16:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f876b1db5bb9c9255bea19ae18fde9747fdb0c02be464e9379fa51c73d2f5f`  
		Last Modified: Tue, 07 Apr 2026 02:16:24 GMT  
		Size: 11.5 MB (11502348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5368ac9a74843c95e70f77bbacac35d2162ffd6aacf13ada3d871c8775775d8`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d920dbb8d782826431dc24219d719874db195b5c3204623b900bed68910d5`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f782acd2f323b11fe0ded7a1fcb099c41b8d25183157922c41891127243c5875`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 101.3 KB (101265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:18247538bfd3db99a32a3758e7d03994c39a2e2ef1595d508fa2dba7ac77fb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302c2b4c9cf24812a3a1862a60bc8b7b80e60f7881845d9fc04d388753327acb`

```dockerfile
```

-	Layers:
	-	`sha256:e04f46240354956e7214563f94cd809be7295aa5e1d169c9b958b714fec79ab8`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fb8255945b9e668090fa3ec96598e2849651c55338c00303b5b49d1bbeedd94`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:86178481890d97f684454ded53c7f45765f092bbc50ff8ce6499015d9ca48ab6
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
$ docker pull neurodebian@sha256:fe085c2b66f5b98b8dabff665c090189b22b35705127c028d99a9de4ea2fbd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d884fcd0aa0fc7742ce71fda5592ddb3bdaa70abcfec2639be95de666e9a24`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:00:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:00:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3652b2041f6d71d5a4d2d4ce03be98853d697f2f28e3747ad8472df52258c718`  
		Last Modified: Tue, 07 Apr 2026 02:01:11 GMT  
		Size: 11.1 MB (11103609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072842f241cf41b2f78c655669448e3045739cc128d4db6f0e65a677f45acd35`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d227b73727a72f1240902141a5dd294aa2e87c47192b9198ef9072bb1e18a745`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d69b4dbfc56c2df58387113855e5cda409a9cbfe3d9e3ce402f3b5df010a35`  
		Last Modified: Tue, 07 Apr 2026 02:01:12 GMT  
		Size: 101.4 KB (101397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d923103343bc5dc334553f01396291d7a8d9d308763f616c40e0ebad605522`  
		Last Modified: Tue, 07 Apr 2026 02:01:12 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5b76ba35ffbf45b3b557b0eb3b42c7cc0a670ebe7b740ff28abc6f767b68d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5908ada024d71ceb6322e907e608c6a0c1ef4c4a62b8572c340c9b61e67b460c`

```dockerfile
```

-	Layers:
	-	`sha256:5b60da26860f07f069517505df7fde872e2c1542956d21035e652d9f1d5511f3`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a009cd19fa2fbddcb46841f1749649b56cda9c9f4f9b995b420d772a73b5d7`  
		Last Modified: Tue, 07 Apr 2026 02:01:10 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8ebafb70a46289d45705b2924366ac85b68c040fc9b4fb0d212b6e1b14f3e47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dcf58c6c976daca65f1d05ca1cbe23a599a739b69de86a428b1cd743704180`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:03:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:53 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83dc7b608ee9f4bda69e556dfafd08b0deb8c7d5b42fa6c452c69fac9069b8f`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 11.1 MB (11109902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb66da7ba94831ac5b43b51d0a0aaf36b8246252e087373ab93e36d45e127d37`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901116b9c6b476b402eba10437d139accc48117e8396221afb2538026b321972`  
		Last Modified: Tue, 07 Apr 2026 02:04:03 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a02b336969d84a4c8e10611b9c2470e6dbfdae6cfae1ef73b5745974d357c35`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 101.3 KB (101300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e190faa9f5e8d05e12f9dbe8984c181f00be94a7d7cfd8b8d4ca3d0c972c97d`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f59235285ee52e1f4c43c5ac7bc42631e373265d406e3a2a873b4ecbc791815d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3628bf8275b73b66b6703f4b0a233507b559112334b32eec23b58647aba7a5cf`

```dockerfile
```

-	Layers:
	-	`sha256:a7ede3816ed841103388f14a094f99b57b7988e98aafe1c9b20aa2ba51ea19e0`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e813811093f9223245e90f6a2c4e5d36513fe28f4694e3d10fca9fe6b70c9887`  
		Last Modified: Tue, 07 Apr 2026 02:04:04 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7579a35afe8e174ec62d633c68614ae8124f1f401a290b9e69c0f62d50a5ef10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66308720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d676756c0d27d5b94529bd4c6cf71c8d72096117fc03c9b367501f8bbc5f3d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:47:57 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:47:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:47:57 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fba7877b3ec8a566d97b730194c65658357ad675cdff2c35c6c1c8b5deccdb`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 11.5 MB (11502302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850a009dd4f23e9a62f33ec76651cd49ec853a8fd4707631e6d659cbd4a056e9`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3ba9c78991f613b0caa3f2f7156d2cb6faf06ac0d6819d4e02644dd1381e0`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97b6b6dfeec66a8cc3a24e834879c3b4d6c1a36922d9d638bd2db930dd40044`  
		Last Modified: Tue, 07 Apr 2026 01:48:07 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59daf1c381bebf5c5efa361f8527b353c71c67fe360ebb066dff44e164e82ab6`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7c5a566c3f8389fb009e31a33132c70c124e29e40a1eaf7c7d2ff15ddfdb3be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440cf12cf83a85140c6cf0ea5e40617e7189077c445023cca2e79d2844fa2737`

```dockerfile
```

-	Layers:
	-	`sha256:3f915c61028bc950f81318a5b1cd11ef596cd314b75ae7ac01ab9084e21f0ca1`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79910c58c46c2b4404c3dde156e9cd6932bbac7116f4d759f11d002c3b02bcb`  
		Last Modified: Tue, 07 Apr 2026 01:48:08 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:ec5c927893e165e413574d4a95fc4aa2bf7daba09f19fc02b9fbae228ddb6cf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:69374892c0ce5a3d9bd103e3b997358c0aa2fb60e06ac8ba2ea3e09bd2b4173f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6787144db69cce1ac94fa4a46bd1cc3735e7e578a4e8704f371e8cca3de11573`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:00:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:00:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecf7ef34f03fc32538b4c6bc3cbf0d01fa667e366f696a2b1b39da8d1d24e95`  
		Last Modified: Tue, 07 Apr 2026 02:01:05 GMT  
		Size: 11.3 MB (11273447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3077df9530666ce829113eb4a39b277d3532c38c6ebb03cfac2a8e95b9cf2cbf`  
		Last Modified: Tue, 07 Apr 2026 02:01:04 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff477a3858b3b073172eb6cbef5c603c6d179fe5c11627c8f92a47ad40df0811`  
		Last Modified: Tue, 07 Apr 2026 02:01:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c5f9e5e22a6c3d7d5ae1831ace77cfc614002176122ba52c76ee3cf1016961`  
		Last Modified: Tue, 07 Apr 2026 02:01:06 GMT  
		Size: 93.4 KB (93395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc14871e80f180acfc726df0095a7322b87ec9ec7c779fdaf5f3902932603a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc52beb3f71dae7afe1a716b1630bee54e197fe4dba13536121e8354084415f`

```dockerfile
```

-	Layers:
	-	`sha256:8edcebcd31c853812834c2af90d7eec07181b1978340cce161bb3caf015945c5`  
		Last Modified: Tue, 07 Apr 2026 02:01:05 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff8fc817494ea4dfad37dd4cb06b2500633f45982649e5054956e53ce4ecd5d`  
		Last Modified: Tue, 07 Apr 2026 02:01:04 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0062560357e6454cca95c4ef20bf2d849b4b3004ff2f7f86bd3f34dd367ff649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0741da89d0cc52e9e35b8a254719a22afcd3e32d5d4591d1e20335186b1a1a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:03:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d1166f044c61640bd82a6fe129d067e7bce23a8dfe007f35bbd3cd6835740e`  
		Last Modified: Tue, 07 Apr 2026 02:04:11 GMT  
		Size: 11.3 MB (11252912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e716b1fa9d2b80c2928865aabcc140f526f471aab2f997e8a02f3968b341239a`  
		Last Modified: Tue, 07 Apr 2026 02:04:10 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402db94ec99e82a9c755850f6f8134a49feb6c9b54dbbdfb03003a9750a712ec`  
		Last Modified: Tue, 07 Apr 2026 02:04:10 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d4ecefa8e2af0fab878d2bb0f4204f37ba290d04d091ccc77fa2387b78658a`  
		Last Modified: Tue, 07 Apr 2026 02:04:10 GMT  
		Size: 93.5 KB (93544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:51978cfc1bdf132867c56497500ec712cc7cfc9fad94fa735554fdf54a88f33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6c0433ea5908d5ff244917a6425460481d58268b3e6eb66f40ed6262276187`

```dockerfile
```

-	Layers:
	-	`sha256:46ca8fbb24a5f8ca822a6a144b7c6f2e1de91320d491c709392af4eca43e1e1e`  
		Last Modified: Tue, 07 Apr 2026 02:04:11 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf45543149a841c10e3f75a54fecfe50d9b9cfd4c8a8952d103d09321a1f3cb1`  
		Last Modified: Tue, 07 Apr 2026 02:04:10 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

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

### `neurodebian:nd120` - unknown; unknown

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

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:eec5743071ab61aa2cf34da2f1e8a57197d04422ee5dc71aafaf4a519125fe0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:af9f36583560add0684ae7dab1bdb816f61d3f044bc5d455d931f4ed617ad22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bdccdb9cea6c7c13ede7ea3a3b75fb283da72406aafbfbb73813d7525d7eb4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:01:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087844227ed0cec1ba8c0d55d16a177a3d958608ac6f329ff2f6c631784c3e92`  
		Last Modified: Tue, 07 Apr 2026 02:01:15 GMT  
		Size: 11.3 MB (11273380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3f71f3b70db64197307fb8014659f0717258a59dd1cf269b297abbf9369a15`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9dbdb0f05f5cc24a2a509c37a8a55370a45ec69644733fa4eccbd4c755aa99`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1ba3fe3df2cd610b2d6f5af43b9f3aac6f36634eea0c736cb6aa176082b004`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 93.4 KB (93372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed21624c95a06c5fd4414bb36c295eae9a954252902d38e2dcdff94cfa1b39a`  
		Last Modified: Tue, 07 Apr 2026 02:01:14 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ac3718cdf216ba5cd7faf127d896fa8317033f3fc6ecd9014408fe6180c605b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8abef2d402a5dae0cb6e2146b2e6bf0521b504d9d1e81d98e3519375037667`

```dockerfile
```

-	Layers:
	-	`sha256:78653761a1692a80ecf22c84ca7bd515ca9da4cf3c2d746a8da1750bdff35872`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9755936729109275be75495c721adc327e6540f8f6bd7bb7b9da1731cfd520`  
		Last Modified: Tue, 07 Apr 2026 02:01:13 GMT  
		Size: 16.0 KB (15991 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:05ae6caad883291c05cf64301ea240dfb58e9ccf487c04dbf125593179065486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578adc7f11a9e18c0f6c3228e563ad98f58d374b38b4e7e76654e19262b20ba8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:04:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5f29ec73e1886510fb1ecfb768935d56a0bdb2f3329b6deaed948e148f6e68`  
		Last Modified: Tue, 07 Apr 2026 02:04:17 GMT  
		Size: 11.3 MB (11252932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73e9830f6c7909f269def0fa09293e5734e8331bf6f21d021aad1d19281930c`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d3bab704f4df2485dc0b8b1b1d11c105ada61e1fd0e6720c102bc1bdc764e`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e3f5f6b18c765c6fc844131a5bebbef69e1f6e26669c44008a1ad65654263`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 93.6 KB (93574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19aaa0d12a3f380cf5dac0e4a3d81d3d55b275b9bcb5768f64d5204af903c03b`  
		Last Modified: Tue, 07 Apr 2026 02:04:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a47a902ef9ae281f356a699f0831cba6bb9248423abbd2b4e7fe6a8620bc720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68838707a3e479a7f2dde37704699cf4149b940ee08843fd666ccd5a39314951`

```dockerfile
```

-	Layers:
	-	`sha256:c6b4f56172d14829f8e80f3225a5350ba9e3e6464cc9b302d06f022d7152dadd`  
		Last Modified: Tue, 07 Apr 2026 02:04:17 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d59339a4f579694ce7b209551f0d3b190faf1b489c5c5ad478ed15dd23159a0`  
		Last Modified: Tue, 07 Apr 2026 02:04:16 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3c724d4e45ca96bebf9f3fe357c4829339b3157a445848dfe46de5eaaae9c3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c734b7942d0eea2f2a08c52e5decee33af22cec203299e20516fd50b63aeec9d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:48:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:20 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9facbaad0d2e9efdf61ecbe5eae48392e462f6157769317a5cd77132fb5b51`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 11.7 MB (11693031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a0e5638a1662e5b018e668beba699060c773c9c9b5033e00982543cde5738c`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414a4c6370804d818b9319fcfa6758e633a7415d496c9365dd0a1f42c514214`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df32f075adbc2243cd6c4ca9bd13113a880f00ca717165e78f34ac340e358b`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 93.4 KB (93398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe93084be076971d6e0edf6f5a7b43f04ecbd6ab6bc01a2f0a3194af7cc09d90`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9e32f6700d0f6d5346a0337cda926a571a48e2592e895b59b79ff9c772ad4934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1be16b2bf72dd8ba11a539af912bd560396aa55dae968808a92678c26e3467`

```dockerfile
```

-	Layers:
	-	`sha256:b6600f485447398b6186abad6be1aa3acad2eb1130b9c7fdc1f47432182bf884`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931719e6ab5e367efad0d917c166131e4686443e17a79f01f0b9072b373d387b`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:2f4c470979405f043d5816a2dba54ca07331e342b4f9a7db2e47a6c3478f43ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130` - linux; amd64

```console
$ docker pull neurodebian@sha256:6c104489228738831d5ca33b6baf71ce5cfc18b9e9f7bc0d14ae6a445dfe0c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3c00b85430bbc08735ae3ead27683573e91bf9af2e8f1dac4561f50996dc0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:01:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491dd2c1ce4a7e4b47bb0f8c8b741e73a78e971f2f0b5f576c0b20ea8c265992`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 10.3 MB (10292926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499acfb1e6832771a0807da2c835d40a0fcf56fa1e829aadeca0574f98e59cf`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3cda9db193172c74664130719db3132d8bbab1895244ff787f388fa27e8be9`  
		Last Modified: Tue, 07 Apr 2026 02:01:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa31249a55d68e978373b17a3a29045fda264a2f48ce4546b00e5c7df843de9e`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 90.4 KB (90419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5013919ccc9ef92983a73ab94bea9b759b6e5d9bc0b349a0c5578a57eb01196d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e767760a21268d05f2acda8a74b7dec0ca65ac8ecab817a8234bb4383d5b57f2`

```dockerfile
```

-	Layers:
	-	`sha256:c537c6e052c78b4e59bd6777ddc6484a9a231f89d686f491afbc066bcf392bca`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f9d0e0748809704210bd279c94b612a1fc365276fff4575ac4651202720d38`  
		Last Modified: Tue, 07 Apr 2026 02:01:20 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:58d1bd7459c21ab1d7a283920ce3c6da18d960096352c0ccf2535b25d1a4250d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8775e554e09da19bca8c4c969d979b5900d0dfc4e5faddca26558b30c893ff2c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:04:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e31d89380ba732a0406195a80e8d1f3739c5ccfd5c102147c23a0a8f4708d7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 10.1 MB (10077988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2483c2d3147352a96a1061695bd50cecf1a77bf57f3a77aac478c02f0f67ef8f`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2751667ba5d31911e37cce1f7dfd23821525fb957928f5faa8a6cdd36d3b61`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420205519c6217769acfb298c60c3c469bdb5371378721822ef809caeae63ca7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 91.0 KB (91038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b30f0489d7276af845415c7260183e991fc4cd8e77740cce7ec7d7e141690b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f8839bd68e19d91358b5a5abd666a7a4e5fbd79c831055c5c36fe6db305ae5`

```dockerfile
```

-	Layers:
	-	`sha256:4ba20350eefa715ad7383f1264c935f46d9475f86c079fa66d4a2a7eb7cb8de7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fbf8fad5f0b3b5169e280dc6798fe61163081b0b66a7b5f3e18062d3ca4f133`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:422c2755b2e1bb2cd368b83e6a6e2c89ab0a54fb5f4848d7e2e4f6a8f220e7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545007a21b6e79e48db521a82a8df542d7e10a15a63e5d34df7a68e6b0e17388`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae1f0fbac6a88be9dcb23c571da82da088cadda19b034b842e84cfcaa28f452`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 10.5 MB (10467068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754115c41d1776cec3df85c51bf394a2902c4eb791f82968f19c476a4eb2c6ff`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f12721908b18e9c6e9b6ceae633014052eeaecf3932e098fd33b5c039692a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0d1e672a9c3716d3995031e1bccf1c7cdfc458eae2a4dc4586cdafed0da19`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 90.7 KB (90742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ca41842e4de756490c8d6ea1114951e8a19bb5e3d1a854c8a444b58430791eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee0777bbabdcec9770ecc591bd196cf2bf6b83641b2694d4bb341221b144989`

```dockerfile
```

-	Layers:
	-	`sha256:df67e9a01457161fed449645509b7c5c64fcb4132915e5ad855cd6dfe596865a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c16755d7777b7d788fb820ba0fc72234a522326dbec9d099a8f50ae45927358`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:b655705ebabaf2ce3541737bb5aa50a434bc498db4e71d21e78df6f65276dd87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2345e9d5aef9bbd8d5fce685c875b87cd8ed38310bdbf275f30cca1737fa3a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d597a16ff660ee441ebb22d3b5bb180c902805200ccf1292560255191a5119`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec6206d450964491a7487cc2c8b4f2d994ef88606a151b06667b29523f578c`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 10.3 MB (10292928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bce8330f04da576bc446171d4d85bc2cb33d4a1a8355f2dfcec201ce53475`  
		Last Modified: Tue, 07 Apr 2026 02:01:35 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529612aeb6812b0c6d4163ca3c7a25ff18656319204675ea597093c2b448ee39`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1c90309da3f2798b43a125418e184e41332d88d07ad27de08314749cbe727`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 90.4 KB (90395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1975e8b7aeb2feea22d9bdd8a88f171e1a11c1c03731143a067e89182c6f80a8`  
		Last Modified: Tue, 07 Apr 2026 02:01:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3499ca84d0540454357e462df180fc71f6ca058f826cc3918bf9199ac4065950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158f867a7849bd7d777618e51b2b411cdf63e44258290d824a82443276cfc38`

```dockerfile
```

-	Layers:
	-	`sha256:02878bf7b801891ae222e99167a7e34c7d90a16ee7df9d50dd57627bc41bfb1c`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93c033b100ba18fa1703dd7a625a3839348e09e6b845205fc3a60e57417137e`  
		Last Modified: Tue, 07 Apr 2026 02:01:35 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:93956c4f4fe270b0360744f841d3e50a69c757291c5adcac1b9cedcd068be733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b510a388077c96bf533603818bbadd3c4d8094ccc4fcfb0a3fbae74c2cdbff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d9f60605ecd6ecd594d2869043d5aa85a244922d2cb11c093c4c62ecbfacc6`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 10.1 MB (10077968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5997a6608cf7f8ac648a62e4bca2bd6165adbaaba00f4e78b3a2cb78035c4184`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d740ad08fd52abbff5ee50f1b915facffd710027e5ae2b07068b9852d643bed`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b8900b668d89259fed01570b11b7cddaad65b3a841629706a527867ad9b0ba`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 91.0 KB (91006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133814aac1502a11214ce7e4da9bbc7c2e1c97e1dc53b1e797ae8dfd4289a0f5`  
		Last Modified: Tue, 07 Apr 2026 02:04:34 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b3afb21138d7ee59554afb0bfedbded2fe517cb2f53227d81caf194f368d301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da62f7d9059d50ef8e12afa98aee31767e6e94fa186aadec735578f6aeb5237`

```dockerfile
```

-	Layers:
	-	`sha256:c342d94d37429180b3af40ac9f600ca6ee9bc518d5e59bf5d7e9f9ac9ae6d546`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2cdc4976db034f9e92a88cb5c57d816d6e961b1fad6db225bc78fd9df421eec`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 16.4 KB (16432 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:cb19cf363ab16c0a4358512bd0168fc0ac29b5a94a664aea4870cc8fb35413d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61380228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9fd486bd8c29504ac708615ad12390f9cf8e63beceab58a078f65b45ead967`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767b01bedb93f2d58ac04f7ac194ac8ba7658652b5f26954b88dcf1de2069b2`  
		Last Modified: Tue, 07 Apr 2026 01:48:34 GMT  
		Size: 10.5 MB (10467061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e9095ff2c86640af37247e8b0503adb4a924a7e77a231fc9a0d5dbe2f753bf`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f12721908b18e9c6e9b6ceae633014052eeaecf3932e098fd33b5c039692a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5012222bd8055762234bf5f4cc28f45026d2d60fa64a2da6df5ffe8d611ade`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 90.7 KB (90728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80e0fa139017e2ce92f74f9470029a9ab27762890d4cfc1136536f0ed6db017`  
		Last Modified: Tue, 07 Apr 2026 01:48:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:464b42572321f94f8cf7a4b02fe3edcaebc6f35fa1a1dda491e647463f400b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db9894f53becac279fcdee615966697296b694d316e46d18297f52df1c09a02`

```dockerfile
```

-	Layers:
	-	`sha256:e9071191f1c485726100f970d753707baf500eaea552b82c0c71459b3e35b801`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9c751f6adc1474b1cef7b2048a842ce49333f2e7257f14d2814990772b8ffe`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:6a9017b3233ca41ed67797e5fa2a865ec242517389843412a4421c57abad4792
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140` - linux; amd64

```console
$ docker pull neurodebian@sha256:9a56929fedae0662326117d6e5dd1e0b2b7cc1349b2cf152a987419e3182fb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60059477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a609d06b9d7f0b4722b4c0037179341c8d091db52c33cf1103a260e0a9b43a3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:01:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a619bb3c1f14c591cc163d929ea3f43df5d6acebdd877fecaacf054d56531b3e`  
		Last Modified: Tue, 07 Apr 2026 00:11:23 GMT  
		Size: 48.6 MB (48587084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d037c825c0e23aeadb006f5dafd902c14d32ef6b778abdb287f93ec185f4afa`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 11.4 MB (11380112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17caa6cf3bd376e27df6ae0c80cf1e1c499cce5c07af7b0f4c9a4b5c99649a0`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce0cd7dafe8e8815c85d2c163d5ee73efaea39c8aa25dfd85fcf04a68c46fb0`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5997db4eaf4518112a9a1ef15b02a9a3ef54aba63befeb30c880c36df3dd9`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 89.4 KB (89377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b7d30b0064f7f6542b44eac4be7c4ff5472243a82a54d0e15439ff1ac405c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a159fa7cae1094bd789db22a82737f1598da8ff91aa7b6a2eedae2ce25757fbe`

```dockerfile
```

-	Layers:
	-	`sha256:08e0eaf65642634d33d2de4b38ef140e63c924edb46b26450537d51af1f384a3`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 3.6 MB (3552027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac83dec5d489a6bbbfb99b613e3b54c0ab6be04c9f9670d0dd7605524640fad`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edb2b53157537c2d2c02dfd8eece602261263f34335795b69eeb92d36f5af494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783523f0adabf2862579080f534b06b40e27599b5393c28a50d158d791522d5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8be2228c7df976aa0c1c2333d6e8d72b206ff7533d4625ffeae3663f7240d98e`  
		Last Modified: Tue, 07 Apr 2026 00:11:06 GMT  
		Size: 48.6 MB (48643356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697160fe466de149ab190bec6e9e1290ade0a79286096e7daa5c760e60197f5`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 11.1 MB (11075013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c36960bff1a2ead8dcab909b24198e7190f9e0116e4fe6e295d76f8078a6b8a`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c1b95f12a1663dc10a0cc935bb1a7e9a7c5991e3e62be7a88b1d82aa3beb00`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a92fcb7587a72995d5472a8ae08413c3262707d6d83ee78a4498382240cca9c`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 90.0 KB (89989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:df205eb13b6222d0b2746f3723e697c01e488e9b92727d7dea12dd97cf3656be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94c537e2f013c3777b8e6ed31123c1a89e866c06cb72480cbd9307cc2cb86a8`

```dockerfile
```

-	Layers:
	-	`sha256:65718c326ca36ce31873d1b5c78aa7554ad5f5bb91e9c8c5367648577e6deec4`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3558012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18963cf37800d3076a9518339af99dd3f02829ab9bc2067ecfe637935cb8616c`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:963e9e111e8de94cf6f0bc0fd6677f10f9d66bfcaa1ab43ea137bbbe888beb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61577258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d79aed3d5d0abe958e1d97fb8c77b27f9058782244428ed88556d34491bd44`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:48:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da53d68ed4a6c93e46a747a177c1be57f4bedc8509f9b442a53b6120f33a247`  
		Last Modified: Tue, 07 Apr 2026 01:48:55 GMT  
		Size: 11.6 MB (11606305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274d6db09e5125c5a1f35e35a167fb6e882923e24a15fdccfd52ae3c59f13988`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e4cdfef32a160c154e91fc59967a8b5ac1c481c4b43b670dd60dc11820f3c1`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9110c7b8d6c12b2a6cd0a52f39f4a960d1d3d9252246c30e1fa606d606b5d24a`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 89.7 KB (89656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f1b6fb33d3cc7c53d4c45383340dff8aa68b2541fafda6f159f57ee8a6edfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f3004b499770aae74ad966f0b5757ca7e53a5920485fa3968c47aebdb71fef`

```dockerfile
```

-	Layers:
	-	`sha256:2a79d047e2b4515eda42e50df12461392fed49171ad04a9ce1f1d75ae60fb003`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 3.5 MB (3549980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3bdd8d104ffc8e688a0c4a90fd13b9f18bcd3cfee4cf483f0a2a5a3114b82e`  
		Last Modified: Tue, 07 Apr 2026 01:48:54 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:eacfbf31285a85424ef93cc6ded82ba2fbe5b986a239fd69488c80f0f710945f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6a2235613045b70910bef31f95d400e4ea728d3d872c3eadf068ad6a5556e46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60059992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc43089ed9146b80ec6df0e482f668dacfa87f89c583de65af75120f18cf742`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:01:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a619bb3c1f14c591cc163d929ea3f43df5d6acebdd877fecaacf054d56531b3e`  
		Last Modified: Tue, 07 Apr 2026 00:11:23 GMT  
		Size: 48.6 MB (48587084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa628479b442faba1c1af937394fb683eb51cbbb599e6c4a61d0da961f2d7b3`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 11.4 MB (11380125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcd0304f3bf7b2e1d0efa613975496c67119b2c9e846c5e0c82ebd89a33967e`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce0cd7dafe8e8815c85d2c163d5ee73efaea39c8aa25dfd85fcf04a68c46fb0`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e561ffd779e9b744ab3a7ec489f3193657675d1cc63c19bd41a103f810ae0d39`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 89.4 KB (89428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162049e1938cb0cd398aa0c3337a92e241d35b71469a0f3b4afdc6d8facf563`  
		Last Modified: Tue, 07 Apr 2026 02:01:31 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ed69fb70e1162ba1fcf7caf8b043e147b224c0d768ac9281501a7da25ba4095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5525b32edfe7cca39b6fdd26484b40000d68927bd7d2b0d0a97afa4ef4c6ee3e`

```dockerfile
```

-	Layers:
	-	`sha256:918200918934c6226e2f5e22c79c036415cd438d8dffa4614ab7774fde9c2f2a`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 3.6 MB (3552063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8743c2342684b499a89a50ccc6eac5a1b7ca15b9de0b45b1483221a3422faf17`  
		Last Modified: Tue, 07 Apr 2026 02:01:30 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ba0014eca13dbdc8c4c9695ee548e42bb17ed8f9a8fec425adbe0fcf9acb7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b39cda1b57a54ebd323ebf1b4371137f41bf6723582d02109b35182b365179b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8be2228c7df976aa0c1c2333d6e8d72b206ff7533d4625ffeae3663f7240d98e`  
		Last Modified: Tue, 07 Apr 2026 00:11:06 GMT  
		Size: 48.6 MB (48643356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b0a86641588b3f119195f4efde642f305d497d115b96e5242a1228f623b53d`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 11.1 MB (11075059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c36960bff1a2ead8dcab909b24198e7190f9e0116e4fe6e295d76f8078a6b8a`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c1b95f12a1663dc10a0cc935bb1a7e9a7c5991e3e62be7a88b1d82aa3beb00`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daedc55759c57539904ad5f302a8d8ac0ba365cada751eb464bce0e48e80211`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 90.0 KB (90012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f8aee6980d05907b17819acc5238181f4a4b97ed15b077d9c94676b52bc1e1`  
		Last Modified: Tue, 07 Apr 2026 02:04:34 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:10828bda83635ab4504a20c3acd44d301d95f70967ba4152cd754792d543519d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc48a161a9fcacbf8106a2b73a2a6a135fbbc570303e482b580cf3e410d897fa`

```dockerfile
```

-	Layers:
	-	`sha256:14e69e855ee2483f98fb85b5ff935450656ad764571383eec285973b6a0ad358`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3558048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbcb49532153075f479fa9e706d3028ce305e2d853eba7e7ffabb7342c1fa372`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9bedad4528e45438d1623fafecc7ebd4869eb410b0dbb85e4a82aef61511431f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61577804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6518c25eacd6983972f820d07b0b03542e361c4746f0212991a4ab16af0c24ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad078a61f6e4be70ba6616078c3a30d7878e3c52bb074b890ccf08d7ba6c0c01`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 11.6 MB (11606394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d033c8c40129bbee090a07f5e1df4ee001c1ff1b1fd1e0e8fea876d4dfefe77`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6602b36874f6c218ec4f391df4b2e6eb6c4bfd9979f4f111c5fa69b47496ba2`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d50765ea499d27dee96965b634aa3a32c0fba2532d7f79e39a9119111c42be`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 89.7 KB (89666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedfedf99f96257ae9c575d353d0f5d352b036e3a8c97cf7a608eb3837152eb`  
		Last Modified: Tue, 07 Apr 2026 01:49:01 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4750e3e14c0f736243e2236c09b7da62c1b16042e8849a8a4da7588e6081eca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3479307f59614f39eb4a0fdeda1168462dd3a6ab17a49e6e26b68882d8a5e8fb`

```dockerfile
```

-	Layers:
	-	`sha256:e0ded4254441e42d507739c92b200d27c9f0e81de4f3ddb5ef6bdc0428724d01`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 3.6 MB (3550016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aea253b22bc3a5f64020d8dc3bdb1ea14d6dc3aeae1db43327b6b9d33432be8`  
		Last Modified: Tue, 07 Apr 2026 01:49:00 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:42a6b56811f661930f4480bc40cbf6e91be055b507c08a3ea9b291429b792e90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:e8903dd5f18cc82e3fb1e884ae1a4746c7738a2847ad86f175eb1b62e70e5d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59724e8c9582356746478c7557741e3e11c464edd6a3e13ee3ab2c3baaeba8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:15:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:15:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b205272ff28d72a83b0c052d9f36b45fadb2a03ffa45596ae8e69ff1977fda`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 3.6 MB (3624564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa7cd09349e4d275f5edb2a27bec22260472d5e3de628b17bcf1264218cafd6`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cfe116cfb8c04dba59ba2510192972d47fca24b0d0b290dc85565c14a7bdf0`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c19e2b3f2b0bfa3e6f4e9f975d5eb097d832a9072d402567e9c26ecfc34a5a`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 111.2 KB (111198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1cfa6f37839f2b9f2fd9efc7f1ab60b9779b0a14e8e7d89d043ae54fa9e4694f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3b7fa07d975a595a59358f4764ec240a8eb7dba0a6cea3228697f3b0843a3d`

```dockerfile
```

-	Layers:
	-	`sha256:714a5735345c61cb4295f36de327f294127309c242243f4166317465165377ae`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f09df083110f0840d2504cde969b323334a83985c62290499a3bf8a26573aa4`  
		Last Modified: Wed, 01 Apr 2026 20:15:12 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:56de5ce50bc6484dfad202db32b89a2f2ca4d48557aa48e4cf11d390d6da73bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913e7ec62ad9077f24a0b24e72ecc4fa55fc5e7b77ce11f79f53bf152cb8eec1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:14:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:14:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f628ca3d20e1c17214b7d1cfb648c745e7ea7a5fc3188f05a7a757a2de998d`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 3.6 MB (3604788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80793066cb18af083cfac67a17a06c1e4afd12ea6ace3fa8f6f8a613d469756`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368eee4161f30a527478029668d0d63de762edb4a59fba3555fa62c09279eed`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3674a38a9279ec2d8a0bb18ed63f4e177a930c5e9be7229b354701d6769b50`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 111.2 KB (111153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:12e4211b6e6d2c9a0ea2b79782e147901a46b2ee80063c345077a1ec63b5cd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8c580742abfd21791b0d471b0ce3169207288db6a9055b3b11eba03a1a593f`

```dockerfile
```

-	Layers:
	-	`sha256:391329d2b648bdb436cd1b6af1bdfc3a3143bfb69f62a4fb083a16013a6ae01e`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31201397be8aef44a004153ad48cb4a0c7c73f929badb242256dcd2610935155`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:392dbeb6af6b687493f63cbc5e1ac017a996efa42b7087014190bdc9ee28d82f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:94ce1db1af85450c8d68a617194541b3ce4701341bd8f5720a7d56aca43c960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f6a6e5468c8cd593f014c698ec62fa71c88440f0d5d42793091a5572e2cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:15:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:15:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d80b2d6b05311b2bf85ebb53e3a2513e5705d12a9123796d1c6ea60554e651e`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 3.6 MB (3624576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ea02e1d1ed6638f377e1e099a7b43e52ef2b4298495dae050273e351d29265`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf0571466a6f5648b0698f0a4be25f95e6b2505ae70977add87cd1aa6c0733e`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78758f11159b40c258ca47ebcc824379dbf5299f8c350a93ee15d41af341bcb5`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 111.2 KB (111203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58eaec0b4361bb71faec94c13bf7b6ba076efef6e254f966213ffabd6815c3c`  
		Last Modified: Wed, 01 Apr 2026 20:15:15 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:92075526fcd071ad41feb014f0acc16d0a42dde119562cd26d47d86713bba3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6b55cd81bb43ba395287c451f75717548124cbb1de94496a18b8f0b6cce6c9`

```dockerfile
```

-	Layers:
	-	`sha256:3a39455db87e67b1acb94e008a6bf7932a50406749255cf986e186fdbd987c07`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7733d7a85b8661d6ba394101ea5f0a1cec8218b5e283652cd2fddaa756ec7ac`  
		Last Modified: Wed, 01 Apr 2026 20:15:14 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:394de8222acd546223af23904aa1ed27bf129b9229cd1870d371c159048d9a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51928ab1653f2d374fa511b1c7850b344a4e33a52a58812c7a8ee6ebf75f6a8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4019784363cefaaa0608f44a7c43404f1b49123f5490bd18ff61d334344dcd03`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 3.6 MB (3604713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac14a880a2f296e4a09554d5f7d84793b55df94e7b4c331567c990b3480470`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7b185bb1d3b8189d1af6df1aeeb5e439b37bb515e3842af0b98424dbe2a5fe`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736213a2d43cf0f24c9174b8fb31963c318bcfb6708f00ace854f394cf5e34f3`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 111.2 KB (111166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57c1c1d3cafd08cbb99d7170a7ed6f9d171ccb1bebae7ca7ed6a66cb514d61`  
		Last Modified: Wed, 01 Apr 2026 20:14:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1c5645de0a996722122f4c9fe0b9ee1feb9f9fa5e235152031b99bd71d3229c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb25718c8f24128797396d2c2b144f786d6ab403adfddb2df3c99adacea0df61`

```dockerfile
```

-	Layers:
	-	`sha256:0957159b9394ba37b209348e8d8a8338cef651a44bbe52536707849659184f84`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8676f87d12d1ed89bca09e6bcafb4093ea3eeaac8b18ba0f5f60591dc4211c78`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:860480ad29d276fd2a4ad492738e5eb7d3b7466505c69146bd983dfe210d13aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:7d1a16f4a7789c0fa50e05f3820f819b5229f9edef5620172f8bcbae486577f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33405565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad82263189b9ddb0b4a213ef9a88bea88681b2a1b7b5ea17c78993ce6628908e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:59:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:59:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:59:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c353de522f5bf7730064fc02df9ca1a7b840cbcb8260acd278a06a132b92ec13`  
		Last Modified: Tue, 07 Apr 2026 02:00:11 GMT  
		Size: 3.6 MB (3564644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9902b56decf65c99d207e2bfa35674e7dba325bd945e956360622539e4a8f`  
		Last Modified: Tue, 07 Apr 2026 02:00:10 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5836d6413083202467f9df4f69b72a9932be44b96e58826746cac34f2d617b4e`  
		Last Modified: Tue, 07 Apr 2026 02:00:10 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a27a2093d1d11303a2baae2fbb490e05fb0b6d1507f222e20019810f15a3e1`  
		Last Modified: Tue, 07 Apr 2026 02:00:15 GMT  
		Size: 104.6 KB (104552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ba3e07af16799c418b33c90a5f2a546656d6d3a05623d03ceba4382dfed4fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca1e85a85595e151c30cc576e3a1e530955df573e022248324dff6565846e37`

```dockerfile
```

-	Layers:
	-	`sha256:f141df93540a232a857921deaf6e34d6410a39ed42b962280edcbd5f569ae45b`  
		Last Modified: Tue, 07 Apr 2026 02:00:10 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32c27b98bc907d2799b42d5c9d8d5d79ae54a89737da34c53f4f618032ba9f1`  
		Last Modified: Tue, 07 Apr 2026 02:00:09 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c8f94a7902924b33b11cd397567eecd55144942719776019db2a3ce38a16a4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32544146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefd438c90cab87ca61c9333a730956c6588e14c4f048d0e0d64dae9299ba915`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a95b347de9e182f3fd87861cb7a8e9ed1fbed7c3a0525130b13c6cd4f8f3d`  
		Last Modified: Tue, 07 Apr 2026 02:03:40 GMT  
		Size: 3.6 MB (3561832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63356e459d23ac85b9482c640aeee2637e648f5345cac58f22b353c015235695`  
		Last Modified: Tue, 07 Apr 2026 02:03:39 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e685769f3ff6ae1a435c2cffac3d43e37d1e4de266dfac553c66102fd1925`  
		Last Modified: Tue, 07 Apr 2026 02:03:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93dc91c1c65bfa3afb57ffc701a23f1eabeac94cd51d24b983cd3741e6678bb`  
		Last Modified: Tue, 07 Apr 2026 02:03:40 GMT  
		Size: 105.3 KB (105328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8a169d4bf32620832e2b29a8ff5797625e29aa64fd04fb758032bf9c29cbe386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbb754eadc6baa9548b6bcd1b4b95eb958be3925bfcc5776bab0af72b07aa69`

```dockerfile
```

-	Layers:
	-	`sha256:e2b613a3a815688d46603d5e1217679bb9e29db75b5a97a47f71e81ec97ccb74`  
		Last Modified: Tue, 07 Apr 2026 02:03:40 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b88624234200988b8d416085ab7877b80d0dcfeea382e619f5bc3dbc24f584`  
		Last Modified: Tue, 07 Apr 2026 02:03:39 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:cbe39f842d9096c1e40d29b2bcde2f331ca6154ac2ce5e9f8c79b176ab13c155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6b55e895ebdd2f79d3658f113ef2f57d67962629ca0f2b2f15870a37aaf9efd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33406032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab01f807b5286ea4789d5ea4bdd8f993605157c76b42460e5fffd9ead2bdefa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:00:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:00:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:00:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0d917224f51d05e6ae0c92305c2602edc21425028f21e1d1f3aadd80d8667f`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 3.6 MB (3564699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c18e2471c46e3c72b1d68c211e53f7049ba7a426dd72ac909b76f9438adc776`  
		Last Modified: Tue, 07 Apr 2026 02:00:35 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41361b01c229b7313f9850623fbed547bdf15ed442e32cb5fc2ae3c8c5f86a8f`  
		Last Modified: Tue, 07 Apr 2026 02:00:35 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7979ca299d86c57ccef385d5f796ea9fdf486b5a376633fc4dd04956740b4f1`  
		Last Modified: Tue, 07 Apr 2026 02:00:35 GMT  
		Size: 104.5 KB (104535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d3ff1ed7d6b97adaaaa5b71a23e6017e5f65c6ae0de4b5b270a69e182bae61`  
		Last Modified: Tue, 07 Apr 2026 02:00:36 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f0c5715fbdd8f8d522848b67fcb6cfd627f92bf4264b6c5272ccaee502576a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817065b62977ea86717dade0ea29f17c2594f5d2f77edb48038707288bf0c256`

```dockerfile
```

-	Layers:
	-	`sha256:3fe8e9d522e4fcfa58979a232cf359ddc838824c28e169e36ea4472d0031e2c3`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 2.1 MB (2120925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2503eb1095db01cdb235ac8354b2bb4905aa3ae3f9ca1f390bb2fcb4c7b3a71b`  
		Last Modified: Tue, 07 Apr 2026 02:00:35 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1c02ed206aab0c1055b6a3e2b538e09cabf9398ecae225e779b6c4bd5149efc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32544557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31a798320ff543b1aa87191cb07ad1e3271f2dc3de24e1bcf887bbb0b4742c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea259aaec9355b4b6af743b21520f1e3caa445e5bbad874b2225b64869fe2af2`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 3.6 MB (3561793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e535061714984df432d30f551ded6165e42cbe4b75fb435254734bf38f5850a7`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25ec071926b31d43f3aef4b681715fa4fc8fec22f179b42213baabb3bc18929`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f856d8180ad02358dc1e650368c564edcc56aebddcb74bfd542bd5b461dc5326`  
		Last Modified: Tue, 07 Apr 2026 02:03:49 GMT  
		Size: 105.3 KB (105348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea053db1dc5ce86955c41d7d294d4aafbe1a488a90345fa0983fff8d3daac39f`  
		Last Modified: Tue, 07 Apr 2026 02:03:49 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a069ab528b8abeabc9b58ff5d560337c6ecc08470aaf32208449210da4d554c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf86f658881f71a38200734c3c50a548972e2105f68f4a9cfc62df90d434a5db`

```dockerfile
```

-	Layers:
	-	`sha256:3c54181484cba7974adeb7f7bf9e6cd4aefcf21e57c02b6bda83728d1d5ccba9`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 2.1 MB (2121970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ffb9d9c2df02ece0645649e7aeb0e49946e5a39939441b75aabfe5f8023755`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 16.3 KB (16302 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:860480ad29d276fd2a4ad492738e5eb7d3b7466505c69146bd983dfe210d13aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:7d1a16f4a7789c0fa50e05f3820f819b5229f9edef5620172f8bcbae486577f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33405565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad82263189b9ddb0b4a213ef9a88bea88681b2a1b7b5ea17c78993ce6628908e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:59:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:59:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:59:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c353de522f5bf7730064fc02df9ca1a7b840cbcb8260acd278a06a132b92ec13`  
		Last Modified: Tue, 07 Apr 2026 02:00:11 GMT  
		Size: 3.6 MB (3564644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9902b56decf65c99d207e2bfa35674e7dba325bd945e956360622539e4a8f`  
		Last Modified: Tue, 07 Apr 2026 02:00:10 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5836d6413083202467f9df4f69b72a9932be44b96e58826746cac34f2d617b4e`  
		Last Modified: Tue, 07 Apr 2026 02:00:10 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a27a2093d1d11303a2baae2fbb490e05fb0b6d1507f222e20019810f15a3e1`  
		Last Modified: Tue, 07 Apr 2026 02:00:15 GMT  
		Size: 104.6 KB (104552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ba3e07af16799c418b33c90a5f2a546656d6d3a05623d03ceba4382dfed4fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca1e85a85595e151c30cc576e3a1e530955df573e022248324dff6565846e37`

```dockerfile
```

-	Layers:
	-	`sha256:f141df93540a232a857921deaf6e34d6410a39ed42b962280edcbd5f569ae45b`  
		Last Modified: Tue, 07 Apr 2026 02:00:10 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32c27b98bc907d2799b42d5c9d8d5d79ae54a89737da34c53f4f618032ba9f1`  
		Last Modified: Tue, 07 Apr 2026 02:00:09 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c8f94a7902924b33b11cd397567eecd55144942719776019db2a3ce38a16a4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32544146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefd438c90cab87ca61c9333a730956c6588e14c4f048d0e0d64dae9299ba915`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a95b347de9e182f3fd87861cb7a8e9ed1fbed7c3a0525130b13c6cd4f8f3d`  
		Last Modified: Tue, 07 Apr 2026 02:03:40 GMT  
		Size: 3.6 MB (3561832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63356e459d23ac85b9482c640aeee2637e648f5345cac58f22b353c015235695`  
		Last Modified: Tue, 07 Apr 2026 02:03:39 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229e685769f3ff6ae1a435c2cffac3d43e37d1e4de266dfac553c66102fd1925`  
		Last Modified: Tue, 07 Apr 2026 02:03:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93dc91c1c65bfa3afb57ffc701a23f1eabeac94cd51d24b983cd3741e6678bb`  
		Last Modified: Tue, 07 Apr 2026 02:03:40 GMT  
		Size: 105.3 KB (105328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8a169d4bf32620832e2b29a8ff5797625e29aa64fd04fb758032bf9c29cbe386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbb754eadc6baa9548b6bcd1b4b95eb958be3925bfcc5776bab0af72b07aa69`

```dockerfile
```

-	Layers:
	-	`sha256:e2b613a3a815688d46603d5e1217679bb9e29db75b5a97a47f71e81ec97ccb74`  
		Last Modified: Tue, 07 Apr 2026 02:03:40 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b88624234200988b8d416085ab7877b80d0dcfeea382e619f5bc3dbc24f584`  
		Last Modified: Tue, 07 Apr 2026 02:03:39 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:cbe39f842d9096c1e40d29b2bcde2f331ca6154ac2ce5e9f8c79b176ab13c155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6b55e895ebdd2f79d3658f113ef2f57d67962629ca0f2b2f15870a37aaf9efd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33406032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab01f807b5286ea4789d5ea4bdd8f993605157c76b42460e5fffd9ead2bdefa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:00:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:00:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:00:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:17 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0d917224f51d05e6ae0c92305c2602edc21425028f21e1d1f3aadd80d8667f`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 3.6 MB (3564699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c18e2471c46e3c72b1d68c211e53f7049ba7a426dd72ac909b76f9438adc776`  
		Last Modified: Tue, 07 Apr 2026 02:00:35 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41361b01c229b7313f9850623fbed547bdf15ed442e32cb5fc2ae3c8c5f86a8f`  
		Last Modified: Tue, 07 Apr 2026 02:00:35 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7979ca299d86c57ccef385d5f796ea9fdf486b5a376633fc4dd04956740b4f1`  
		Last Modified: Tue, 07 Apr 2026 02:00:35 GMT  
		Size: 104.5 KB (104535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d3ff1ed7d6b97adaaaa5b71a23e6017e5f65c6ae0de4b5b270a69e182bae61`  
		Last Modified: Tue, 07 Apr 2026 02:00:36 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f0c5715fbdd8f8d522848b67fcb6cfd627f92bf4264b6c5272ccaee502576a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817065b62977ea86717dade0ea29f17c2594f5d2f77edb48038707288bf0c256`

```dockerfile
```

-	Layers:
	-	`sha256:3fe8e9d522e4fcfa58979a232cf359ddc838824c28e169e36ea4472d0031e2c3`  
		Last Modified: Tue, 07 Apr 2026 02:00:37 GMT  
		Size: 2.1 MB (2120925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2503eb1095db01cdb235ac8354b2bb4905aa3ae3f9ca1f390bb2fcb4c7b3a71b`  
		Last Modified: Tue, 07 Apr 2026 02:00:35 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1c02ed206aab0c1055b6a3e2b538e09cabf9398ecae225e779b6c4bd5149efc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32544557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31a798320ff543b1aa87191cb07ad1e3271f2dc3de24e1bcf887bbb0b4742c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:03:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:03:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:03:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea259aaec9355b4b6af743b21520f1e3caa445e5bbad874b2225b64869fe2af2`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 3.6 MB (3561793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e535061714984df432d30f551ded6165e42cbe4b75fb435254734bf38f5850a7`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25ec071926b31d43f3aef4b681715fa4fc8fec22f179b42213baabb3bc18929`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f856d8180ad02358dc1e650368c564edcc56aebddcb74bfd542bd5b461dc5326`  
		Last Modified: Tue, 07 Apr 2026 02:03:49 GMT  
		Size: 105.3 KB (105348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea053db1dc5ce86955c41d7d294d4aafbe1a488a90345fa0983fff8d3daac39f`  
		Last Modified: Tue, 07 Apr 2026 02:03:49 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a069ab528b8abeabc9b58ff5d560337c6ecc08470aaf32208449210da4d554c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf86f658881f71a38200734c3c50a548972e2105f68f4a9cfc62df90d434a5db`

```dockerfile
```

-	Layers:
	-	`sha256:3c54181484cba7974adeb7f7bf9e6cd4aefcf21e57c02b6bda83728d1d5ccba9`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 2.1 MB (2121970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ffb9d9c2df02ece0645649e7aeb0e49946e5a39939441b75aabfe5f8023755`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 16.3 KB (16302 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:b655705ebabaf2ce3541737bb5aa50a434bc498db4e71d21e78df6f65276dd87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2345e9d5aef9bbd8d5fce685c875b87cd8ed38310bdbf275f30cca1737fa3a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d597a16ff660ee441ebb22d3b5bb180c902805200ccf1292560255191a5119`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec6206d450964491a7487cc2c8b4f2d994ef88606a151b06667b29523f578c`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 10.3 MB (10292928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bce8330f04da576bc446171d4d85bc2cb33d4a1a8355f2dfcec201ce53475`  
		Last Modified: Tue, 07 Apr 2026 02:01:35 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529612aeb6812b0c6d4163ca3c7a25ff18656319204675ea597093c2b448ee39`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1c90309da3f2798b43a125418e184e41332d88d07ad27de08314749cbe727`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 90.4 KB (90395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1975e8b7aeb2feea22d9bdd8a88f171e1a11c1c03731143a067e89182c6f80a8`  
		Last Modified: Tue, 07 Apr 2026 02:01:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3499ca84d0540454357e462df180fc71f6ca058f826cc3918bf9199ac4065950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158f867a7849bd7d777618e51b2b411cdf63e44258290d824a82443276cfc38`

```dockerfile
```

-	Layers:
	-	`sha256:02878bf7b801891ae222e99167a7e34c7d90a16ee7df9d50dd57627bc41bfb1c`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93c033b100ba18fa1703dd7a625a3839348e09e6b845205fc3a60e57417137e`  
		Last Modified: Tue, 07 Apr 2026 02:01:35 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:93956c4f4fe270b0360744f841d3e50a69c757291c5adcac1b9cedcd068be733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b510a388077c96bf533603818bbadd3c4d8094ccc4fcfb0a3fbae74c2cdbff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d9f60605ecd6ecd594d2869043d5aa85a244922d2cb11c093c4c62ecbfacc6`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 10.1 MB (10077968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5997a6608cf7f8ac648a62e4bca2bd6165adbaaba00f4e78b3a2cb78035c4184`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d740ad08fd52abbff5ee50f1b915facffd710027e5ae2b07068b9852d643bed`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b8900b668d89259fed01570b11b7cddaad65b3a841629706a527867ad9b0ba`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 91.0 KB (91006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133814aac1502a11214ce7e4da9bbc7c2e1c97e1dc53b1e797ae8dfd4289a0f5`  
		Last Modified: Tue, 07 Apr 2026 02:04:34 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b3afb21138d7ee59554afb0bfedbded2fe517cb2f53227d81caf194f368d301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da62f7d9059d50ef8e12afa98aee31767e6e94fa186aadec735578f6aeb5237`

```dockerfile
```

-	Layers:
	-	`sha256:c342d94d37429180b3af40ac9f600ca6ee9bc518d5e59bf5d7e9f9ac9ae6d546`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2cdc4976db034f9e92a88cb5c57d816d6e961b1fad6db225bc78fd9df421eec`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 16.4 KB (16432 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:cb19cf363ab16c0a4358512bd0168fc0ac29b5a94a664aea4870cc8fb35413d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61380228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9fd486bd8c29504ac708615ad12390f9cf8e63beceab58a078f65b45ead967`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767b01bedb93f2d58ac04f7ac194ac8ba7658652b5f26954b88dcf1de2069b2`  
		Last Modified: Tue, 07 Apr 2026 01:48:34 GMT  
		Size: 10.5 MB (10467061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e9095ff2c86640af37247e8b0503adb4a924a7e77a231fc9a0d5dbe2f753bf`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f12721908b18e9c6e9b6ceae633014052eeaecf3932e098fd33b5c039692a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5012222bd8055762234bf5f4cc28f45026d2d60fa64a2da6df5ffe8d611ade`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 90.7 KB (90728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80e0fa139017e2ce92f74f9470029a9ab27762890d4cfc1136536f0ed6db017`  
		Last Modified: Tue, 07 Apr 2026 01:48:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:464b42572321f94f8cf7a4b02fe3edcaebc6f35fa1a1dda491e647463f400b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db9894f53becac279fcdee615966697296b694d316e46d18297f52df1c09a02`

```dockerfile
```

-	Layers:
	-	`sha256:e9071191f1c485726100f970d753707baf500eaea552b82c0c71459b3e35b801`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9c751f6adc1474b1cef7b2048a842ce49333f2e7257f14d2814990772b8ffe`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:25e9be42321ebefe6ba08a0c5d941df090d2943c03c2af4cbcedf72afdd26120
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:6d1e2474b98c2a1bcce15b241a355af4da64ec06aa918936617898d29512ac25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60171574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac865a5fabef498174fd27d645f2ae8be8b6b6fde69f727b75846321f55cfc7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:01:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b208148f3abde07a5ac47cf579ac1ed4c9312d2ae485addb285765d8008fe12`  
		Last Modified: Tue, 07 Apr 2026 00:11:41 GMT  
		Size: 48.7 MB (48710648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9680cfdd3e4129a60748e1904e29c37d431b0b864e26b6cc1169ffebee2cb75d`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 11.4 MB (11368683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d3bef65c117797166ff5ed760c078a32b15b167e32a553a29c940570822487`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aa0f33df95aecb126fa27d57bb3a070b44e34656956e7fe0264b009211d5c`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d45a5729852586277730461289592c04d0e6dbb72de0e324fbe2aaa4ed9d4b`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 89.3 KB (89340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:963260a04a05bbd3ebd62d35d0e902a265a373f9de3ed9623ecb6cd28dae7f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1362085b857b4acba8f4275e8aac5c6c836e3fe86647fbe51b6e62fa976a2c`

```dockerfile
```

-	Layers:
	-	`sha256:1fe4067892c99e2cf5bc78a6bd50a625130390f8b50c68533758ac6f5af8cde6`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 3.5 MB (3549087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a3533b60c61480c4ae00331be5f79ccbbc42761982e303d6ad716012bf7c297`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:31470d05e1cac0a1fc11d2a656a7e2d8dc2144bf2a61a17deef16a5c76919400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59910208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bde8d257c76a0907a0d9b72dc78d5c7e23faafdcd8a3d208dbc5a33e2bfa443`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ac9c76c00b1b19d9057c64eebc87efd57976d9d3d4373752703081335cbb1900`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 48.7 MB (48744945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17966fa7c8589dcf8dc631f45556cd118e6cfdd3792e0d613548c653c7ba358`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 11.1 MB (11072457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945ff9025edf778838c09cc7ede3fe6e4d78195d9a5d83e9a08d56f48b8a57dc`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5466b442dfef5b49389002c7e3ad8b9c512754b0041f963eb9a349bcd89b8e23`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0177b69925e015ec37347d8c984b1cdac4793c06f8deb29a244711fb3acc3df`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 89.9 KB (89905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:59f0686f262a5e90c82fe3ffcd59f58fdbd4fabde77ccc91b6ca3abec5aa3dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9527f078cabafd1d52505d1cdcd3bc968dc8970d9f7b252090e846771bc23c71`

```dockerfile
```

-	Layers:
	-	`sha256:1b37a51526a10036207dc61b7842830789c3a2421a4eeaf39bd1e53632363669`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 3.6 MB (3555072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0362e5d5c5cf674f3f001c0ae6249f64af6a3f8970763d8d641c0b28c56cccd6`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:c60db7eec078dc52dc2c3c428344e9aa3479b05011d9d5b163e922dcabe8d9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a656ef86060ebfca5428834bdfca9780b93a6289decfe8dd3876b08d4ad85a5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c3a3fef3f09f7a3e83440b35d7d0f2f724470aa7260920183b022678103935`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 11.6 MB (11602235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53125d28144aed0499a184d660c37574f5dc0488d48921247a3954c584682c9`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca2c3c8f62c3c8516fcb39ee0b67f5091ffee2f35935228425aa07bf9763596`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a659b6eeb646760fd0e9d056438b39521d4fbbcfedde6dddfb7eeef1e8767a`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 89.6 KB (89635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5c2f9498331a592ff803623a19243947488e9062f3f57380e234383c343586fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5a868a104e8cfb4ba4bbc83480a466a971b55003ae7fc8a98d712b25c1e30a`

```dockerfile
```

-	Layers:
	-	`sha256:a58c065d6365faaf3bf8884ca4bf9f13bf2e669f9f981055bbf69409b235f0f9`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 3.5 MB (3547042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be546487457e10b6f2e2f752a781790dd2d55b4764632002fc8e7b752c8b4268`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:24e14e1b58a1807440bcda71183138921fe9bde3590d423cbe3440c61a75259a
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
$ docker pull neurodebian@sha256:6a97ce654e0eb6552d2bb76efc3454ead70afe0a3fc2fa654673e187757038ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60172027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a82e705f83fe881c5e5f192d8010788c9bda962a056898feb36bb82f4f4b26`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:01:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7b208148f3abde07a5ac47cf579ac1ed4c9312d2ae485addb285765d8008fe12`  
		Last Modified: Tue, 07 Apr 2026 00:11:41 GMT  
		Size: 48.7 MB (48710648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e359a898b31b0e9c8c58f608eaa36be1b8c82ba572cd885ddc5b74e54fa00d6`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 11.4 MB (11368694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd15120090ef6e6a2c1358a10ea832b710c945b4d206662782e92c9eb53a2fa`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aad35ffc48f0873d152bab616af660e071c2abeeb01fa91ce78f73e038f5db7`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7f82a3b3c524294cb678870650f0f1daf178c7144dc185a3d53d63e878ebfa`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 89.4 KB (89363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f0c8526602a286d241f56054e7a00313cbc165ad25f708608ca9977783b8d`  
		Last Modified: Tue, 07 Apr 2026 02:01:45 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b53f533863a2d01b3271f410c55bbe4efb865cbd221fdbe4302e9cdeafd15e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacff77bbcd6b5fcec98b0420bc413e3a4f66b7cd8564c4a2ae88b63cdb57a66`

```dockerfile
```

-	Layers:
	-	`sha256:f57d844cb34d7a636b5e7f9214efc0f0153dc056af5e3dbf29c2f46a067bc9e5`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 3.5 MB (3549123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beb01c446a636d846ec76ef42de8f855540cfe404fa11aaa94e5977b15beae3d`  
		Last Modified: Tue, 07 Apr 2026 02:01:44 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9c61266570716a76fa4d66983ae408d5eea38ae55812bce1046eaf473ed9b647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59910666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de0c61091b23a1980030577b83f83fabb42b6738b3662f056ef9049f88e3748`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ac9c76c00b1b19d9057c64eebc87efd57976d9d3d4373752703081335cbb1900`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 48.7 MB (48744945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85840404f57afb5787eae44f30186f8ebdedf22f7341260a6d562a2e16e6d27f`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 11.1 MB (11072472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf44374b898e8eaab4fef95f90b0e127e4f6eed7b5bbf963f568241a8fb2e36`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c14cd1ddb0b2f50fea0a090beb46755df524ebce2f44860805c804bada8407`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7c94331ed393d89b3a0b7e290ccb642a59a75c1f15fa8c5bf35faa73cff651`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 89.9 KB (89925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38896d5a61d5211f6261adda86c26527050e97d2538d0838ac55c5cecec9002`  
		Last Modified: Tue, 07 Apr 2026 02:04:41 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bac54ec2ea8eb1dc276e26335cc80a4a48ef1c43293159e45895ff1de30d0bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b089d25c53dca863e9b1b12b678ab6f783254e946af06e2e5f07ce7f16f001`

```dockerfile
```

-	Layers:
	-	`sha256:25c5712129944c709b840f4168586b4a685e4b2c4688d661d19a9dd73dba8215`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 3.6 MB (3555108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f09c4d225542d79fc824670a13b384c9c0686035eba21c64e7146ddff3ea29`  
		Last Modified: Tue, 07 Apr 2026 02:04:40 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:379dd6cda62c5f956daa4957282d12057faca8d0d2edb10eb00b63aa4b127649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61688954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4690074633fe4fccb4c59a578a84a38bfc055cd41d859f3fe6750c62c03075b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbde13ff2785b11cd70a92d1da45b61ee2c39ba77f505a32b6764e1bb1f3464c`  
		Last Modified: Tue, 07 Apr 2026 01:48:59 GMT  
		Size: 11.6 MB (11602276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8a43f3df2ec92648d7f9cb6ae9b59596ef7550e9b2c0de212a9d5067d70eda`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8292b280ecf08c2a53b62734b37ab925c0596e7c8837ab862f48b6ed13161a18`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4fd33efcb827f079f283388221dcec47472439dd679e48cc1dd8c9c469c885`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 89.6 KB (89646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee066862e919913f4a8149190cef898dcb0dd51f675a1b0b66cd695eab88dc5`  
		Last Modified: Tue, 07 Apr 2026 01:48:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20806508b55568c0a85953b30cecd0be318bf1353380d952b6c350c1f23b2cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58350dbd42299c78510c7b6d6e14c04f9e9925d1c2ea28148368a9e35ce4182`

```dockerfile
```

-	Layers:
	-	`sha256:07eb593648572153e5a66df88d45281816a4595bd6859d58ff20b91cf3e389b3`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 3.5 MB (3547078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60adcebb1386384577e15e4ca93b84d41693ee7655e05bbf56de36d0fc4ace0`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:2f4c470979405f043d5816a2dba54ca07331e342b4f9a7db2e47a6c3478f43ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:6c104489228738831d5ca33b6baf71ce5cfc18b9e9f7bc0d14ae6a445dfe0c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3c00b85430bbc08735ae3ead27683573e91bf9af2e8f1dac4561f50996dc0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:01:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491dd2c1ce4a7e4b47bb0f8c8b741e73a78e971f2f0b5f576c0b20ea8c265992`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 10.3 MB (10292926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499acfb1e6832771a0807da2c835d40a0fcf56fa1e829aadeca0574f98e59cf`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3cda9db193172c74664130719db3132d8bbab1895244ff787f388fa27e8be9`  
		Last Modified: Tue, 07 Apr 2026 02:01:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa31249a55d68e978373b17a3a29045fda264a2f48ce4546b00e5c7df843de9e`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 90.4 KB (90419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5013919ccc9ef92983a73ab94bea9b759b6e5d9bc0b349a0c5578a57eb01196d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e767760a21268d05f2acda8a74b7dec0ca65ac8ecab817a8234bb4383d5b57f2`

```dockerfile
```

-	Layers:
	-	`sha256:c537c6e052c78b4e59bd6777ddc6484a9a231f89d686f491afbc066bcf392bca`  
		Last Modified: Tue, 07 Apr 2026 02:01:21 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f9d0e0748809704210bd279c94b612a1fc365276fff4575ac4651202720d38`  
		Last Modified: Tue, 07 Apr 2026 02:01:20 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:58d1bd7459c21ab1d7a283920ce3c6da18d960096352c0ccf2535b25d1a4250d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8775e554e09da19bca8c4c969d979b5900d0dfc4e5faddca26558b30c893ff2c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:04:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e31d89380ba732a0406195a80e8d1f3739c5ccfd5c102147c23a0a8f4708d7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 10.1 MB (10077988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2483c2d3147352a96a1061695bd50cecf1a77bf57f3a77aac478c02f0f67ef8f`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2751667ba5d31911e37cce1f7dfd23821525fb957928f5faa8a6cdd36d3b61`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420205519c6217769acfb298c60c3c469bdb5371378721822ef809caeae63ca7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 91.0 KB (91038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b30f0489d7276af845415c7260183e991fc4cd8e77740cce7ec7d7e141690b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f8839bd68e19d91358b5a5abd666a7a4e5fbd79c831055c5c36fe6db305ae5`

```dockerfile
```

-	Layers:
	-	`sha256:4ba20350eefa715ad7383f1264c935f46d9475f86c079fa66d4a2a7eb7cb8de7`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fbf8fad5f0b3b5169e280dc6798fe61163081b0b66a7b5f3e18062d3ca4f133`  
		Last Modified: Tue, 07 Apr 2026 02:04:15 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:422c2755b2e1bb2cd368b83e6a6e2c89ab0a54fb5f4848d7e2e4f6a8f220e7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545007a21b6e79e48db521a82a8df542d7e10a15a63e5d34df7a68e6b0e17388`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae1f0fbac6a88be9dcb23c571da82da088cadda19b034b842e84cfcaa28f452`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 10.5 MB (10467068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754115c41d1776cec3df85c51bf394a2902c4eb791f82968f19c476a4eb2c6ff`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f12721908b18e9c6e9b6ceae633014052eeaecf3932e098fd33b5c039692a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0d1e672a9c3716d3995031e1bccf1c7cdfc458eae2a4dc4586cdafed0da19`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 90.7 KB (90742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ca41842e4de756490c8d6ea1114951e8a19bb5e3d1a854c8a444b58430791eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee0777bbabdcec9770ecc591bd196cf2bf6b83641b2694d4bb341221b144989`

```dockerfile
```

-	Layers:
	-	`sha256:df67e9a01457161fed449645509b7c5c64fcb4132915e5ad855cd6dfe596865a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c16755d7777b7d788fb820ba0fc72234a522326dbec9d099a8f50ae45927358`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:b655705ebabaf2ce3541737bb5aa50a434bc498db4e71d21e78df6f65276dd87
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
$ docker pull neurodebian@sha256:2345e9d5aef9bbd8d5fce685c875b87cd8ed38310bdbf275f30cca1737fa3a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d597a16ff660ee441ebb22d3b5bb180c902805200ccf1292560255191a5119`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec6206d450964491a7487cc2c8b4f2d994ef88606a151b06667b29523f578c`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 10.3 MB (10292928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302bce8330f04da576bc446171d4d85bc2cb33d4a1a8355f2dfcec201ce53475`  
		Last Modified: Tue, 07 Apr 2026 02:01:35 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529612aeb6812b0c6d4163ca3c7a25ff18656319204675ea597093c2b448ee39`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1c90309da3f2798b43a125418e184e41332d88d07ad27de08314749cbe727`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 90.4 KB (90395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1975e8b7aeb2feea22d9bdd8a88f171e1a11c1c03731143a067e89182c6f80a8`  
		Last Modified: Tue, 07 Apr 2026 02:01:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3499ca84d0540454357e462df180fc71f6ca058f826cc3918bf9199ac4065950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f158f867a7849bd7d777618e51b2b411cdf63e44258290d824a82443276cfc38`

```dockerfile
```

-	Layers:
	-	`sha256:02878bf7b801891ae222e99167a7e34c7d90a16ee7df9d50dd57627bc41bfb1c`  
		Last Modified: Tue, 07 Apr 2026 02:01:36 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93c033b100ba18fa1703dd7a625a3839348e09e6b845205fc3a60e57417137e`  
		Last Modified: Tue, 07 Apr 2026 02:01:35 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:93956c4f4fe270b0360744f841d3e50a69c757291c5adcac1b9cedcd068be733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b510a388077c96bf533603818bbadd3c4d8094ccc4fcfb0a3fbae74c2cdbff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d9f60605ecd6ecd594d2869043d5aa85a244922d2cb11c093c4c62ecbfacc6`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 10.1 MB (10077968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5997a6608cf7f8ac648a62e4bca2bd6165adbaaba00f4e78b3a2cb78035c4184`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d740ad08fd52abbff5ee50f1b915facffd710027e5ae2b07068b9852d643bed`  
		Last Modified: Tue, 07 Apr 2026 02:04:32 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b8900b668d89259fed01570b11b7cddaad65b3a841629706a527867ad9b0ba`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 91.0 KB (91006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133814aac1502a11214ce7e4da9bbc7c2e1c97e1dc53b1e797ae8dfd4289a0f5`  
		Last Modified: Tue, 07 Apr 2026 02:04:34 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b3afb21138d7ee59554afb0bfedbded2fe517cb2f53227d81caf194f368d301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da62f7d9059d50ef8e12afa98aee31767e6e94fa186aadec735578f6aeb5237`

```dockerfile
```

-	Layers:
	-	`sha256:c342d94d37429180b3af40ac9f600ca6ee9bc518d5e59bf5d7e9f9ac9ae6d546`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2cdc4976db034f9e92a88cb5c57d816d6e961b1fad6db225bc78fd9df421eec`  
		Last Modified: Tue, 07 Apr 2026 02:04:33 GMT  
		Size: 16.4 KB (16432 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:cb19cf363ab16c0a4358512bd0168fc0ac29b5a94a664aea4870cc8fb35413d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61380228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9fd486bd8c29504ac708615ad12390f9cf8e63beceab58a078f65b45ead967`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767b01bedb93f2d58ac04f7ac194ac8ba7658652b5f26954b88dcf1de2069b2`  
		Last Modified: Tue, 07 Apr 2026 01:48:34 GMT  
		Size: 10.5 MB (10467061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e9095ff2c86640af37247e8b0503adb4a924a7e77a231fc9a0d5dbe2f753bf`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f12721908b18e9c6e9b6ceae633014052eeaecf3932e098fd33b5c039692a`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5012222bd8055762234bf5f4cc28f45026d2d60fa64a2da6df5ffe8d611ade`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 90.7 KB (90728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80e0fa139017e2ce92f74f9470029a9ab27762890d4cfc1136536f0ed6db017`  
		Last Modified: Tue, 07 Apr 2026 01:48:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:464b42572321f94f8cf7a4b02fe3edcaebc6f35fa1a1dda491e647463f400b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db9894f53becac279fcdee615966697296b694d316e46d18297f52df1c09a02`

```dockerfile
```

-	Layers:
	-	`sha256:e9071191f1c485726100f970d753707baf500eaea552b82c0c71459b3e35b801`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9c751f6adc1474b1cef7b2048a842ce49333f2e7257f14d2814990772b8ffe`  
		Last Modified: Tue, 07 Apr 2026 01:48:33 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
