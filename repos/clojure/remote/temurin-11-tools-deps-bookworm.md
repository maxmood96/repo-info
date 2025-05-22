## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:71000112013183ca6e5202618e4b4c226e7391c70ab92e6f182dd163ad1a4b6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5da5380e4b413894a750182be7b071fe3e70f18448394f65adcb7d4958261b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275119578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0bdc12eb6a59c09209fcc8618e877375afd7d1b1d4715aff3d1b3ac4b5bee9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d422aaca88411f296f86121286899d79d1fcbc7e3c0a5a8f16372016a229ce8`  
		Last Modified: Wed, 21 May 2025 23:32:32 GMT  
		Size: 145.6 MB (145635749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9209eebde0cf4e3049930da8b63dbda29d96976af1973be58126ae5f4203a6b`  
		Last Modified: Wed, 21 May 2025 23:32:35 GMT  
		Size: 81.0 MB (80994940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6863f987cb88a69681cf847b6393d8c781f1a5673b889aabf56e021cdbed16`  
		Last Modified: Wed, 21 May 2025 23:32:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d25666b2a20f0b2f93d58a548b5241830cc90b09ba0597ea76fae3b0d7cb07fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7252915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc48ef06459eb2d5c9d5ecd47789bf63ca0e5938b305317fce50fd9464253eb`

```dockerfile
```

-	Layers:
	-	`sha256:f5afefab26efdf25f37d449dcfff4b2657ecd293cb86fa88626101ea1803b7e6`  
		Last Modified: Wed, 21 May 2025 23:32:33 GMT  
		Size: 7.2 MB (7238663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752c658e7b3bbb99c270952ce9aeeb4a35ff559956c2b89c03c6d962e92e5dc2`  
		Last Modified: Wed, 21 May 2025 23:32:33 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:229b51ad4d408285dab83e4f29cf2746f1eb4f90be185f97a096c3a0f6d91698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271595211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbaf50ca33ef02fd14b548b4ba6efef78f8cd63d6fc5c4ac0d08c209dc0175a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682800a477954fe07fd9e841558f511dffb10fc0892f35d76669df1d97081e87`  
		Last Modified: Thu, 22 May 2025 08:09:34 GMT  
		Size: 142.4 MB (142420720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a014d244cc693a83ac405a6d68fbc8e67d1249a0b41af04a62ebe3299ef251`  
		Last Modified: Thu, 22 May 2025 08:14:38 GMT  
		Size: 80.8 MB (80846666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b2bd3fdec57256481b3482f92480dfe32b075c2137078d20baa065a0846a68`  
		Last Modified: Thu, 22 May 2025 08:14:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:90c327b34bf60ad2cfb5983ce879e31f0bc08451c07eae08161a332f96e0a7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7259414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b845fef0302fe242db6de12b419ba99aebcf70e51714b374d7b087546889304`

```dockerfile
```

-	Layers:
	-	`sha256:69f936ba4cbb6100e62dd5e25828ad68416de89b54b47f720d86f13cc8aa41d9`  
		Last Modified: Thu, 22 May 2025 08:14:35 GMT  
		Size: 7.2 MB (7245044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c09a6860148eb828829542aa9198fcbe5964840b321015e4c234ac27a5bd374`  
		Last Modified: Thu, 22 May 2025 08:14:35 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:80b4cc758206165317d17feef1e80d572b3bd18906257695adb9a11f59d7825d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271943093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac01d90331f1fe7db0c2cd699f487f5624cd51635c4fbc5d7882b230cd46a49`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d25aae9e978e4525cc2180fc5318000690790b0d71ee34b6794b179ada9fba2`  
		Last Modified: Tue, 13 May 2025 18:24:30 GMT  
		Size: 132.8 MB (132809861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6047a689f83e85451d6a0cc65b9aebdd61492dff799b5a9333d5f3c8926e7da3`  
		Last Modified: Tue, 13 May 2025 18:38:10 GMT  
		Size: 86.8 MB (86800459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b595dd988f626b0699dd43da0e3c2c9e02958cc1aed5c44057e9cb2db9c607c`  
		Last Modified: Tue, 13 May 2025 18:38:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b3694f790541a3fa695c11674d1518ceea64b8a62c6adc0d81dbf973bbfcd4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069b345c6ba9e58768daeb5968926ad74d3287428af8742cfd162b7058882bc1`

```dockerfile
```

-	Layers:
	-	`sha256:608251b52815e5e3f03b4e20dd64b6389677c7e98d504a36c9acf8d535d929d5`  
		Last Modified: Tue, 13 May 2025 18:38:07 GMT  
		Size: 7.2 MB (7197044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c974ee28be39913271f7c5ae9b1bec6d821af4232fb57f61d39d1d13ea4b90c7`  
		Last Modified: Tue, 13 May 2025 18:38:07 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:dc907caf57083efb700f581f0f24169a30e25245c9727e8dff7fcc68736f3950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252520674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf65e8d29935af89e04bdcdd5fdc38cc5fbb60ce16d43c300aa58e2c8d1c082`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198a062fba45f29a5333d576680d0e7c053156ddc38ef227e0cff249525620b2`  
		Last Modified: Thu, 22 May 2025 03:38:42 GMT  
		Size: 125.6 MB (125585847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046b020127f70e52ad265a59098ecee1d81075ceb02de55de36f886469243b7a`  
		Last Modified: Thu, 22 May 2025 03:42:40 GMT  
		Size: 79.8 MB (79790342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9479c3b4c94305264374c9fad4b5a0235a4ea9fd954ec7d28d139293051fa396`  
		Last Modified: Thu, 22 May 2025 03:42:38 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f38fe88ab4026eb571dc6bf7f224440f2fabd340640859c978bb7765ecab75ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7247130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0246faceb7037a9f40a15ed8b3729ced94e7ba4fea943a3ba1bf314bb10552f`

```dockerfile
```

-	Layers:
	-	`sha256:21d073bb408ed81ad3356a04e700e414fb4071b2bc76dbf3bc873312c3095836`  
		Last Modified: Thu, 22 May 2025 03:42:39 GMT  
		Size: 7.2 MB (7232878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872b82cec68160076794d83285e65d08a2873f735b2bedbcd9463e3ea5aba7e3`  
		Last Modified: Thu, 22 May 2025 03:42:38 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
