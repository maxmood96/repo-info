## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:4ed9cc2cf914ddd0ed3eca8665578f3c822ed32662d5c4fba7f3a10be8f7ed62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dcfefe382046f15e76b701fb93647a816e61aed2d098779136f9a370f19caae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246209014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6318913c014bef4d005762261fe247645e62c776f9cc7d9cad04b4f7565daaf5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eae6d19ba162079402bcc9a2237cc5b6f146bdbb178adda2de7923ba14b11f`  
		Last Modified: Wed, 02 Jul 2025 04:17:10 GMT  
		Size: 144.6 MB (144635030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ad9257fa223cad4847ac2fa2bbf7617e3d5b6303702f187cf6644bf0a938b2`  
		Last Modified: Wed, 02 Jul 2025 04:17:27 GMT  
		Size: 71.8 MB (71811838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba473110234f6fcdf3b44ec4a10c97ad370606a0de6925cf602cedd74e0b990`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b28f6974050760016fe95b4dab7f03d3c5988ed98eb08d4098a927033e25151`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:34c73892eb5576f740e143b8f34c4e2cb32960c02957c6fe2c343c9550a06248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f020dbc221febc18e96815b2690279391c0a7b225b4ff08bb62917481b4b120`

```dockerfile
```

-	Layers:
	-	`sha256:20cbaed44089b33d460f04be89f9244c82a25a5545e62862a4f9dd0c03a9af8a`  
		Last Modified: Wed, 02 Jul 2025 06:38:54 GMT  
		Size: 5.3 MB (5252802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3458bef1216d0ef18e03858d5141afc8ba443298bf109061e8adc65b47a1d3`  
		Last Modified: Wed, 02 Jul 2025 06:38:55 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:76ef17e9d10a62c488a249a4718d33dec6ee03713e3c7bce01cb483038c3ef1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245281789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f52d5bf19079065e0220ea013a419344d10f7ad163ed248c4638b732e63137`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d08ab08a45fba1b01cd568eba49c6cc56d5c5b1bf1fb8fb51dce922b5278a07`  
		Last Modified: Tue, 01 Jul 2025 12:22:25 GMT  
		Size: 143.5 MB (143512615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ea6120bf648bdd77a1a918cd02c0518f8d5bf627ef2251588f375b1158d9a1`  
		Last Modified: Tue, 01 Jul 2025 13:00:09 GMT  
		Size: 71.6 MB (71641271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d503809bf4b5fb8c5a714c5e96e8d10cca3364ced0a5f398e8e07e5fe9daf286`  
		Last Modified: Tue, 01 Jul 2025 13:00:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56039890fb453e0a9e3e380babb1ea7001c5f57a9ed5328427b1999b0ae9104a`  
		Last Modified: Tue, 01 Jul 2025 13:00:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:607191d61709fd20e5fd2b687bf1e906967de250162d59f8da63e7dd33af4765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22a1c78c3ee979c33e7d298ca52ca4c67743fff4115172f02569a848065aff5`

```dockerfile
```

-	Layers:
	-	`sha256:274566b11fd46429768d7f25a29293129fb2db7a7880f3af5a887533a158aa90`  
		Last Modified: Tue, 01 Jul 2025 15:37:59 GMT  
		Size: 5.3 MB (5258571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71cff36bd39ce28a6850763ebd8955e9ef4fc2d8f6ee941b809f08ced1560938`  
		Last Modified: Tue, 01 Jul 2025 15:37:59 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fdec0565d740bff777c04674ae849aa556890b3425f2b37e77ebb9014dca7a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255100412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c47f4f9b7bbe67acff823ecbd13e55e54e52792d05ddab5d68270f77841fe3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7c76c33e89d8d234c685147ef17003512fb41891617f72e9998041e1838c54`  
		Last Modified: Tue, 01 Jul 2025 13:31:44 GMT  
		Size: 144.3 MB (144280554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b42f33bf832b6d376981f2187ac140819d9f28894d56e083c12010f25f8c57`  
		Last Modified: Tue, 01 Jul 2025 08:54:45 GMT  
		Size: 77.2 MB (77232780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f5622281b7cc4ba7499d0fa5207f2f209ac33cfe88b0ec40b34b9c6040de1`  
		Last Modified: Tue, 01 Jul 2025 08:54:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cde9a48b94f7f67d315ca0946b9c4b1ad29ccf9da9ab7489f08e7d53238a068`  
		Last Modified: Tue, 01 Jul 2025 08:54:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff2488c6381e047f16995fb6e1139a452866eb5e2faa1c2af318d6a9894c219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ef966b3f9d14a482011f528bffb007303b3e386757125acce3c658468918ed`

```dockerfile
```

-	Layers:
	-	`sha256:9510b346977ec7b4b4b3e0267fd82cee2712530c460b11dafcbe648902db6cde`  
		Last Modified: Tue, 01 Jul 2025 09:38:41 GMT  
		Size: 5.3 MB (5257173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a91649fe4ce469a383c9ec6b4dbe84d7e6bb4796711efb37228a08185ae902`  
		Last Modified: Tue, 01 Jul 2025 09:38:41 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6800ba5204859a554016d1a8c2fcb3a1ccb7480c9febdf6797a643b2b040f9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237455547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10262c089cbe8dac5eabe1ccb7767201d391bcb288faefa4f509e92115dafbe2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:43faa9a2f25436afce0db8221e3c0e223102f73a33b0cd47eb32294e8033b203`  
		Last Modified: Tue, 01 Jul 2025 01:24:44 GMT  
		Size: 28.3 MB (28258970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b044d6ffc3783b16fe8050c13a2002d45e9199e735ad5aaf6c25079b6f8e3aa`  
		Last Modified: Tue, 01 Jul 2025 13:32:13 GMT  
		Size: 138.5 MB (138492480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c55972de57a689cb30e2f11119a7ceb3c54754967c4d3ca43e06a7e79cc2a69`  
		Last Modified: Tue, 01 Jul 2025 02:54:58 GMT  
		Size: 70.7 MB (70703056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a20455306b7f6f8c94054ed149f7e1b757ab58cf58bd0036003eb7bf4de8a3`  
		Last Modified: Tue, 01 Jul 2025 02:54:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc227a071b1b5be079617ab445cd7b04e2256e5c23b2c12b851ad9470754aac5`  
		Last Modified: Tue, 01 Jul 2025 02:54:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9c0cca3af9f804daed32bd5463450a7ca88c21558bd677399372f31f4ff339e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5256250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf40ca4485e728f8b82c5350012d3f93b5c740afc080f7f991aacedd309902c`

```dockerfile
```

-	Layers:
	-	`sha256:c4fffa71e30b696b779eedd2eb30e9f912c7849565dcddb991e74bf6c2346698`  
		Last Modified: Tue, 01 Jul 2025 03:36:16 GMT  
		Size: 5.2 MB (5240347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83cef6c8b3e92df7229a1a3aa932654cf5c66e3ed65190ba12eff4901f6c9169`  
		Last Modified: Tue, 01 Jul 2025 03:36:17 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:96de0ac9b58adc4922369c289d585392791f6a8adc1d487bb58a1699df1aa31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237315265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6fcfe00d1e4741961d9506768ce3bc0c4906bc5753733bfe7f22a34da5b736`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45862aa2123546ffa489bdc843a3498ad23f176c0071dd028fb28da9492e803`  
		Last Modified: Tue, 01 Jul 2025 13:31:48 GMT  
		Size: 134.7 MB (134673559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544e47612e4268952f9ca2abf5286bd5f7f36549782f91206924bfa22db66f3`  
		Last Modified: Tue, 01 Jul 2025 08:16:40 GMT  
		Size: 72.8 MB (72802324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b97fdcb36095b92df41fc94098993b0e71c4554a8f322ef5b2c9d6bd804f08`  
		Last Modified: Tue, 01 Jul 2025 08:16:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d7a50405132f3003d2bc183563dc7d65c09b0a0d05945fab5cdde651fef65`  
		Last Modified: Tue, 01 Jul 2025 08:16:35 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:84d5c435188e02bb39c93b251e08187a851621ab0d88ba6612e7e9712319ca62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc6f51463d4b06a49b391808a17559e0e3ae78a697389d8daa3d58f869fc62d`

```dockerfile
```

-	Layers:
	-	`sha256:46d41ab723d16634f0a3563a41a523dfb51f460f15a439d42c4fe50861c4fd01`  
		Last Modified: Tue, 01 Jul 2025 09:38:49 GMT  
		Size: 5.2 MB (5248726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ff821feaba534ff8773b0044318bab55fa0dd3398dd70863116c9b72c1f8d2`  
		Last Modified: Tue, 01 Jul 2025 09:38:50 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
