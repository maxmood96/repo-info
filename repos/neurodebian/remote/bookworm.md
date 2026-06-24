## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:29bde8be644f7026cc1e9f4867f569779b90428092b818e4b04953b3f621b08e
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
$ docker pull neurodebian@sha256:702519373b570bc7233efdac094eaed23fe3b98cbb93ece3bb6a0cfebbac68f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59871250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3346755083f53a28ba9b1fdf0e4dac8243899838da46855f3c2a33a6b4459642`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:44:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:44:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000a44c0c78ea880259a3a16691211eca328cb2ea6eef9f8a4aedb0fc757367`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 11.3 MB (11273460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e19346b2023e14a41b3a629a7f131bcb464db229ef6b6e521d273011271d29`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4a539e6f96d095250a8d049480c813499e8fefa60b1c70d73ea0434bbbf018`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953e1654a8a9259b2ec8b027925909627e2e92526d32b87f5a3ac5333792aa18`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 93.4 KB (93406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e6977ae82f6a649e6de5acdde8687d6e8b27685189d22541e87655ce813de064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b335b960f1f2c337893bcfb8633e3e7ee0dbdecf9db03ad1c636eda2df34446c`

```dockerfile
```

-	Layers:
	-	`sha256:17ab0798df44bb649b8b1485000abbc9105d93e69e9993e70e9f3a7b97965256`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76a3881eafbb0a463cd67f4e9200eb1647a027f7d757ad8ed0a39599f247746`  
		Last Modified: Wed, 24 Jun 2026 01:44:59 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:47123181987e52ef981cfc5f7d75a17df2009656b0dfd20321f52e5dbf6adbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59737697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0432667e276c1f96a58ad559d013ee8547e585ee6ac984de02db5e06dd8b04e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:47:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a735ebda1e0cf248011c01a7676af282efac17cec145ba6e198c0ead226a04a8`  
		Last Modified: Thu, 11 Jun 2026 00:47:31 GMT  
		Size: 11.3 MB (11252911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3cd29dcf4276f3390bb7c591a4b35e0db081a8ba88fc8ba2e0c2c37ef3ac4d`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d3622219a2a21ed6e957b57d9177dc02dd5859ffea8adae6dbdb315b7b5545`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae554063421f6d5273c9bf4d90ff55c337368094d308c785ff3ecc37f680628`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 93.6 KB (93602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:032fe2cae497ecb4e1bf5c8fdae524790d8b0fae9a6992eac2fa672eb10c14c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fbc693151be7e6a990a99eb3f13a04f175a8958f517585bfe910b2816f799d`

```dockerfile
```

-	Layers:
	-	`sha256:0ce295b9ec41e4b2923bfabf2680b01575c86088cb8d940538e8990c1d24ee2a`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbbff94d7b81988058a9e96b4d083f4b6c305bf5f90a75982d002aa3c6a0b2ca`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:007a99edd7753df67ff50043632a55393ce7660a2539cefd4ce294bd33e3bd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba4921fdb00b37961f495e202b635ba55549351e142fac3fd8410c735ad69f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:44:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:44:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:44:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96cbacad9c1883b9ae87f68a0550ac0bd7e0b7ba2b15b142a793b89b5a5f36ad`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 49.5 MB (49491378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7058ba24da67d9c6203ecedbaa8d84fccec092ff57c19e281dba766b418c9d`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 11.7 MB (11693184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab2266aad1a9c343d326e16a32b9959738f3db6aa15de817328749c626a88c9`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85808ea636bebb0c873f995758d9c72b988066043f040414cf42e6d583eaacd`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0f317b450af5ec002523cdd104b04639efc63cc32f93a047d43ba332675c53`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 93.5 KB (93452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44c97f363ab6fef57a756f725fa6c4a927ec1ee43f760da4bfa4c9245685162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6557ddbac964b4c0a500ad0b08468a672fad0fecf11c4a80789143161f1b18`

```dockerfile
```

-	Layers:
	-	`sha256:9e38593ce321451d93744ae4adee0614bc19b8ed6c640bbfd38c49e769fc7e24`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1234996d8894105e4ce1b2e6888638254f204e9321e72a8926ddafb65d14fd2a`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 13.9 KB (13936 bytes)  
		MIME: application/vnd.in-toto+json
