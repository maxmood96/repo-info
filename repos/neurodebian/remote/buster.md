## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:7bd34c33c19350f5e1fa77f535923b7850a1410d2d87eb6a6254d03314e7d889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:020104f3971254f7e7ecda9d7906735733e55360f142eb78dc36c229471ebbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61070627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc56267455d2457752fbd7f8ef9bd1351f76f73d7f36ca0755faf9bdea833d8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723d87c39a56b2dd8a62649501bf04ba3a687a53896c94468000a095aaed760c`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 10.3 MB (10307517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1e2e602b28270d610b56d107afb7c3d4e767a70a6b91da844db452b91eb293`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d822bf0f40147d3330203054210369cf3c5dc3a52c16fc1726e82cfc84284616`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222234ed4691c00c09d259495a67f1e32ba942cd3f8c73cfff42245ad61d1327`  
		Last Modified: Fri, 31 May 2024 00:56:51 GMT  
		Size: 104.2 KB (104212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:69131987bd6fe23325f21f49abca3952217bf6bb8340de090f82c2c03bbeb54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903b524f67be676e0a9620c5cfcaf385fb91379bd7be09e955dd7462a04a1ae0`

```dockerfile
```

-	Layers:
	-	`sha256:f1656c8c3a6eaa5e531f96856c15c839a51124b4c946824bb634826eae237680`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 4.2 MB (4215066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8cec8865692dfd27d4aa16a39200a8bcc72abbd0269f2d814dd2579901ab2f9`  
		Last Modified: Fri, 31 May 2024 00:56:50 GMT  
		Size: 13.4 KB (13399 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:176ea7c06f6ea8f6ba781055db94356ee8143d00476e2f10e2e0afd2ff1535c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59872536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03153f64313411fe1da52555de68c42bc9ce00711b014e5fcc7da41d4f2415e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd9c59acf204c0d81aff8b7e5da56cc3b76c258fa40d482df9e225cd533596`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 10.3 MB (10313209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cc3300b9846c0e9c7dba482c8c981db848d2eeb56f74c62c65a1debee89e29`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60fd2e75c963791cd3b0929bb3c01c7671ec64f140a3ac83cf1212b4a5b5c4b`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e238e2f4604a403218d3037f6bf35bb3d8d7e071f2dba1a6a88fbe012a1abb1`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 104.2 KB (104250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11acc36e9dc4881113c767f319b6fa4d3a7951225685756f733dbabcfce3c12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4228926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148c1afddd6bfd55467d4fe9da6aff8cdba3fbb67af8bc72b7f4db65583f8219`

```dockerfile
```

-	Layers:
	-	`sha256:c35575c2bbac68ddb1615f970a8ea5b91b80b162309aa73763693bc47d9e9daf`  
		Last Modified: Fri, 31 May 2024 14:42:04 GMT  
		Size: 4.2 MB (4215248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd5cad799d6f740a31955a3760590f73309e4d2879e32da05907813655385ac3`  
		Last Modified: Fri, 31 May 2024 14:42:03 GMT  
		Size: 13.7 KB (13678 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:buster` - linux; 386

```console
$ docker pull neurodebian@sha256:408c3e1cd2f443916e857ded1382dc93f85b34a19964bfe25d293f2fd8dee173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62198132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4331f3d4bc117e2a005a9d84cee8627ac2d2e49f54b6995083016dc0a620f286`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:5e59addfe8663b7c16cce40874c2a3c8601e20e80f5a0897c86b64ba463c10e9 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a892f56e4b10aaecbb51b3219d90bd0d8a1e955acd0624a6ef27ed086ba168c`  
		Last Modified: Tue, 14 May 2024 00:53:06 GMT  
		Size: 51.4 MB (51419713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c69bf1688c8418e0a4181c9450d35a9e1a4be76cc447a0655c971bbece6817f`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 10.7 MB (10672299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f57c540aa2c151a92c082fe61fb8d24cc3122c024c083590fcf2a67d607e5c4`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e324ca101e0ea13d957f5a45d94621cb084dffaf4547471dd53b306ab98f49e6`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326d790e3e3814d94b6f80ae03b479cfb649503eece3652d4a8c8e3d2a48d31b`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 104.1 KB (104135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:buster` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9e49372b57f4428e4144ec1b4be8b737435f2679c31fff55773cfffd1eaa2327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dca39fbd6bd4f26828d0721e504cd9202d1f1836b6794cb1dece3effdab7b19`

```dockerfile
```

-	Layers:
	-	`sha256:3951d6843c389685fa1ca30f3285aaf65fa2ea7485922c26d3a4f871aa49d36b`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 4.2 MB (4212312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7485ab859fbe734b3354d296b359244784d852ca5562cae306426317aa533ef`  
		Last Modified: Fri, 31 May 2024 00:57:01 GMT  
		Size: 13.4 KB (13376 bytes)  
		MIME: application/vnd.in-toto+json
