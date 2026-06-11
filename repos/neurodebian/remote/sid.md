## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:a9029e6a72e36bbbb4518cf24bedfb9496c67d6b3bdb0358ded4ca2610202a61
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
$ docker pull neurodebian@sha256:ae287380c24223f57660150b7da71cdf4eb84270f620831b0d4efac16f74bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e26bb2b04a99e8f535ff8fbed986163a3ee4d770e5e51d70b77820d74abe0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacf64a88439387b1c0eba23bcec29b6672837e395a0256976be744e995b3bad`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 11.4 MB (11400511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a7e10f751eff090cf764c44d9e5001c1570eb8ebb01f32410ca89370ebe19`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac08f4684991e1cefeb83a94bca5bd073dd502e21dba3d833745e37cff385d`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf49cc7e499d5a430ab888113f99e87e81e51393c55d0894e75cc2769295e6c`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2fd3e58ad348dcac794bb0741eeeb37199ca52fda2ccf9b746d91970d2dbc571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8420cb3d0490b285b0fc8a31fc14d839e9c7aad6895787277fc06946bf1e51f3`

```dockerfile
```

-	Layers:
	-	`sha256:90f7545d094de3aa23907f01f890bc1935142a968c4e73f6e4fe2f64f889331c`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 3.6 MB (3561769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b880c5f3b746d7c60d4781081d48c83adc6a95cefdb282dc6a4fb808c6148f`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b52d4611b34a2bc915f7402bf07b7c0ed611ac77167147a1fa579671e533f20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60005272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8e718cf8135c7a7dbaf28de21e4a599de708b5e737331e8374f470d67a4325`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:48:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:48:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:48:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f216cfca8681658c5c6a7a8b3653ba38754d80730e4760fa07c5af0c77dbafdc`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 11.1 MB (11093783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c245f33d403e20631db07d85c7949c38d447f59151983e6ccd177844c70b2da`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f20446e70687694e58be96b1e8dee8abbbffc8a86361dfef1e2c9933a7e172`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c777496248e833ab9ee2388720300b95430fe7f379a711f6d0d603d2bb9dced`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 90.0 KB (90032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af5bdee722473dfe53afb51c4052273ce01321dc38891ad423a777cd3eed1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e931479eeae972f6d3393eb1fc52d4600aaed088476de284ac64185006b8aaf7`

```dockerfile
```

-	Layers:
	-	`sha256:c667f4c018696b0a60c8e913790fd50a5b7b27861cbb09b150589add99b16396`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 3.6 MB (3566474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0311325e77f970962d6ac2bd4c71cc3ede59589e9266f3b563c2edb9fff8ae2`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:80ab709a5003e5bb19b5298fb94704be677eeacae57e1546f3a27c134e408a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61734334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ac3ec238f09fca3619da6c12e8411fbedf0953b46cb91f86aa5f9046836c0a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:26:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7753854dd3eda9aef2aaa8ce9d1e3f65ad0732a1084526b6ea495204123445`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 11.6 MB (11625732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80680d0e09afe77e520bc718136fe080de719a24960af381889b5325a007ced5`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc9462b033e2edd695c438057a9d245ada5fc84587ca3a58b07feee07ab51`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad603d2e8d78ab42ac28bace917a076937246df7f6d0c0633126b17f0cadb7`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 89.7 KB (89692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:57343788c201a8c001feffcd753e8cfbb1a6dbad640af928c8b65079937916d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583407654d7c95b5dd7f0c49b8cf2c3dda7a02034c8aecaa2c56a63e3009e10d`

```dockerfile
```

-	Layers:
	-	`sha256:d09a0b84829b224ad027b6f9b437d39c2e73c8cdb44870c4ca0bc993869b1c1e`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 3.6 MB (3551313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcef60f7d04efbb4e57e855b92a9b8620465376f9df755c28290b9aa572be599`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
