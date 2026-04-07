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
