## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:d5fbbf1d3617d563d782bf01503fbd1fef4355c1b7bea10d576e7596406234e9
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
$ docker pull neurodebian@sha256:809c477909cf0fd18862b329bcdd4e87adafffe89bcc78c78595b136288209bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a248704bde343620eff25ad63058e527698b855779e7f60b33c85dbe46976cb4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba70e2e27460d417e9bafe489b7e8aecbfee3ab542cf46506db9e6933daf424`  
		Last Modified: Wed, 13 Aug 2025 00:19:31 GMT  
		Size: 11.3 MB (11266801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63dbb5cfed31f01ce53848be77e54f1b827372f4f336a7c17220a0682a3465b`  
		Last Modified: Tue, 12 Aug 2025 21:27:08 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca51e6585eff85a1a04cb4dcd11ea131bf89d28182a044176afb364ae99f1025`  
		Last Modified: Tue, 12 Aug 2025 21:27:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7d1b4818e582a5e2b6e1bdf16e516015dfdcdb7942a5bc6f77e835fc94a109`  
		Last Modified: Tue, 12 Aug 2025 21:27:14 GMT  
		Size: 93.2 KB (93176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2873c836c1cf047a037ddbcb4567dea2943db0b58175712744910b6ce7dae032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2e783ce35e1e95e612539402f6e4ea65d2e012e60536da62a6b0cc44bc9188`

```dockerfile
```

-	Layers:
	-	`sha256:e3a460b4d5d0a3f95c812400f1f36520eaac5ac80142b4917b38bf49dc39c2ec`  
		Last Modified: Wed, 13 Aug 2025 01:07:20 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f05668a5ab1c144345b5041d39371123218559d76cf9a2a838e95fcf44290c3`  
		Last Modified: Wed, 13 Aug 2025 01:07:21 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c8475a51e84b66e3ce6821ff7ceb84eac7fc1f82c048e7e402cc67f417f8d8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59670712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ced994f26f2b092eb62ea23fe3fe8a513dbed97dbe77e57534e99512f27578`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398157a4590ac7aadba659d655fa1e00f8f05a8ab0784529d0099545f337bc03`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 11.2 MB (11232652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e01fcd5942424056ba8f0b9a313ff0dde95202c4e3440076fc637b0813c64d`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8405e7c25660e800db97c97594d0a4f9b537b1a9fc32793315de1592d0bcfdb9`  
		Last Modified: Wed, 13 Aug 2025 07:32:56 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2527f69d856843d89ea49d0ee163b7a03c78ceaa2f858c3cbaddacefb732357`  
		Last Modified: Wed, 13 Aug 2025 07:32:57 GMT  
		Size: 93.4 KB (93433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:95aa20c2049cfb33598e143e3edd5dc301fed6cc15d10b15e12b05d5fecef4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95975f3930829ee9652fca1f4c3fab3c5ab20a4725720748de2d91c7d54024e9`

```dockerfile
```

-	Layers:
	-	`sha256:6924f68a66edcd1f5082dd813dc5a36f4913133252276abcde4364e8df649299`  
		Last Modified: Wed, 13 Aug 2025 10:09:27 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d38ebd5108b733f20fdcc43249cf599fddb52780aa4f43dfc91df35dc80cfe4`  
		Last Modified: Wed, 13 Aug 2025 10:09:28 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:f84316ff8d8b3ae225ad8c0d7e7e45491b919bb56181dbca5ba1385f3e635cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1819902dbe75b0cccf9bab3c758cf24bbc4c18b666d86310ac25e446f66a16ff`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
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
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0557245a4233d6ed0a813738d93888d73d43eb684d18ea929937431c9702`  
		Last Modified: Tue, 12 Aug 2025 21:21:37 GMT  
		Size: 11.7 MB (11688898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73e78c8ed688b9fec478bd057658df7aa8c559e4b5bf882be1c175cd08163b`  
		Last Modified: Tue, 12 Aug 2025 21:21:35 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9193997ad9c823abe8f7d1c1f448e6230c212498a20cdb047aa0dfeff48e673a`  
		Last Modified: Tue, 12 Aug 2025 21:21:34 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7d9601317c4ff1f530caa3ac9c137a87432186a6f634f0acce8c4aadac4c01`  
		Last Modified: Tue, 12 Aug 2025 21:21:32 GMT  
		Size: 93.3 KB (93261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d80795b60339edcebddf5fd87fc6f61602d687c266d903a8b56456a56d0dcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415d1bbbfd7acae7f60115ce66fac55d6a6b2e5f2cab7a30a0363cf67f53b124`

```dockerfile
```

-	Layers:
	-	`sha256:046403f77b477f1e3e1a5f4c7ab21e86bfac80b32b641e05560f049f6b3f4b2b`  
		Last Modified: Wed, 13 Aug 2025 01:07:30 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021a0daf0fa67e89ec9b08cb19b9fa33fe27b477bb7fb2afc77ab8732d68b0fb`  
		Last Modified: Wed, 13 Aug 2025 01:07:31 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json
