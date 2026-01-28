## `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:016ff67b144c18fbc2552a2314287e3c5e6303a3ce3c6c22b1797e7613af5df1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:280b11af1d780140e0bbb618f3ee9a7f097a05667012ff7bba65b7ff6b58651e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178032171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837db22c9126b046283bfcc9f6f2d991cd388efcbead1e43f0178de39cf3d3c2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:03:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:38 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:38 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90951b23f75a9b97414bed110563f0719599e8a5e8739d353c98a3a5e537843`  
		Last Modified: Wed, 28 Jan 2026 18:04:26 GMT  
		Size: 54.7 MB (54733370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffa8233f9f7ad4d493a16b908cb3f6ebcc5837f7859fd43cb8ff63faf96b1c0`  
		Last Modified: Wed, 28 Jan 2026 18:04:26 GMT  
		Size: 69.5 MB (69541708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0554bf2d87c413769847ab473fdfdeb0dddf9c8740aefde72c1d2aeeb3eeada`  
		Last Modified: Wed, 28 Jan 2026 18:04:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9a67323e6c250526b6f339e5ed73e2743f8531d3a214a03b879435467bce5f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7532270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765e54a6e270244b83cbfed4201a2959994dfce42e5d77227fc9aa317d939271`

```dockerfile
```

-	Layers:
	-	`sha256:972f0cea907b98824b65718e565ebce05fb0159e1c1b7d806b4e596800447f9a`  
		Last Modified: Wed, 28 Jan 2026 18:04:24 GMT  
		Size: 7.5 MB (7518076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da93df0c2e55930f7b3a7ea4ad86f42b7ec58c192c7467503c1a8204c6571874`  
		Last Modified: Wed, 28 Jan 2026 18:04:23 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f5dcc5ee57b0560f5973bc11aa701e74f4202480acd7e039a74d0f01011d6851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175766486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e3c7cfb06828f7bf76cf6dc7a83c3038f88512defa32689f6dacb1c2126c37`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:02:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:02:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:02:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:02:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:02:12 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1bf7b6e72b57232c45c2a9ad0972a1849a535a7f762cb680f4d280724c3405`  
		Last Modified: Wed, 28 Jan 2026 18:02:45 GMT  
		Size: 53.8 MB (53815013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a004ee6adc404996ce37daa6fe85892f1ec3fd98bd9af2b89f638536cd7ad85`  
		Last Modified: Wed, 28 Jan 2026 18:02:46 GMT  
		Size: 69.7 MB (69693058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ecd7dcfbd8dabd76146f16ff38ac12e52ccd18b1a1e903da3fe366adf3dd6a`  
		Last Modified: Wed, 28 Jan 2026 18:02:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e6f3dca0646a9e5fbf82b3069b35c452081f5f94c09fbe9703467abe4d5c90a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7538185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5d4b91e841eb4a382ce88a921426830fc4ae6fac9d2bfad2dd4ebad7ca6edc`

```dockerfile
```

-	Layers:
	-	`sha256:7437e423c7ea60291c2a84dd33a9256f10ada51d223bdf0cce65de6ab687c97d`  
		Last Modified: Wed, 28 Jan 2026 18:02:43 GMT  
		Size: 7.5 MB (7523873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:754319cde1b2ca5207dbe5082139f0305548af2d5d8877b6aeb2bb331ccaabca`  
		Last Modified: Wed, 28 Jan 2026 18:02:42 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
