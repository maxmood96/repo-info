## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:2cde096dbeac1fba0c6729246605418d6af83504d04dd54b8b1876cf9078dbf8
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

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:0f3afd925fe2cafa5a90167f3e68f79070a6a7bdfa307a8bffc00ed269c608e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287438565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9260cebf079e7ce380fb8e389955d66df4bf5c3ffb11c27ccc7e06d2e4c6f4db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeebba9abffdc44495b8a2baa28c3480f2f5c837ce1c3e9dec833b7bc075eb46`  
		Last Modified: Tue, 02 Sep 2025 04:32:14 GMT  
		Size: 157.8 MB (157804821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fe5535ed310d033f1fd696ab20f95b9c9d0def63ecf0ff92033baa8d7be6e9`  
		Last Modified: Tue, 02 Sep 2025 01:56:16 GMT  
		Size: 81.1 MB (81138188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d9e890d5eb181405f58d579df0f7c1194c8393e642c8963327a1e5483a0e32`  
		Last Modified: Tue, 02 Sep 2025 01:01:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c05ddba1f3c9e037bd8f6251f54a84194747a2794ce2623964e3fa01272e4c`  
		Last Modified: Tue, 02 Sep 2025 01:01:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:e88059013a2c4573d50db144c9f7c35adfb5cf03e8f39c9194a7ffe38e86ef39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058344a9c6f46ec42c08b97ef1a3066337f6dd90395bf225cbeedcb4559ac4c3`

```dockerfile
```

-	Layers:
	-	`sha256:da3400ad56563cbeb86d8a31169bc5f4291612ec7b4e74d2460a89f8b25e887f`  
		Last Modified: Tue, 02 Sep 2025 03:40:46 GMT  
		Size: 7.4 MB (7373399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3ce4426df3fce8075dc86af473c5537846af084fb9dffba2aebf5368d8d09`  
		Last Modified: Tue, 02 Sep 2025 03:40:47 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7f9514dad288137717e77853b1dfeddc786056526f116b5d3d7d864e64ad88f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285434058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7923e0186787c650956d9b69d8a49494b12e55899378587e8dab01264ae30`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f78888ab9c57e95226c3244d90e801f0c238e605329f20de72d1f2676edd7`  
		Last Modified: Mon, 18 Aug 2025 19:02:08 GMT  
		Size: 156.1 MB (156081244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205c07254b8c53a7d97a9035f701a958d2dab1d4e867144cd9fd36532550dec0`  
		Last Modified: Tue, 26 Aug 2025 17:48:07 GMT  
		Size: 81.0 MB (81009318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21f6665b407306a983bc0579a04e40924af81610feebe03b253643ca343283c`  
		Last Modified: Tue, 26 Aug 2025 17:47:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96419ea193fc8fd244e5b78cf2b6b0343e22fa8611e9c906871b6bb68fda0548`  
		Last Modified: Tue, 26 Aug 2025 17:48:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:d63310d67a17e28556844dbba30471f132c9d71c2d639bed66021124ff90123a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a85c6e01f1e251f28ee6986ca7f8087ff54fd3e844fdc385cf70d1c47d469c`

```dockerfile
```

-	Layers:
	-	`sha256:6e85cf7bc8e6d5993c7dd90db5f708c60bfdf883ec2be232875032bb44e6f245`  
		Last Modified: Tue, 26 Aug 2025 18:39:45 GMT  
		Size: 7.4 MB (7379234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7d59ab69afffab718aac9f220bbec50f27ca534016126f80b7cf11a1d0055e`  
		Last Modified: Tue, 26 Aug 2025 18:39:46 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:264204194fe7ccb9691d7c4206a7557e3ef2463b5601c9606b9fdf32172cae00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297275390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232de03eb48ef196277cc6d36e5eefd1685873b0b6760b6390cf79a84ec5ed33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21178e342602edd12ca410499981adb42800eb941f19d77cad58cb797945aa34`  
		Last Modified: Wed, 13 Aug 2025 22:01:26 GMT  
		Size: 158.0 MB (157963474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e33b25faeddaedd56d237955b1d8704c3e5726b3d03e54c231305f0da8d7f`  
		Last Modified: Tue, 26 Aug 2025 18:05:10 GMT  
		Size: 87.0 MB (86972794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8451491ebeef5544187d4211fbbdad7deb87708f14b9678be35d49a988fa096`  
		Last Modified: Tue, 26 Aug 2025 18:04:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499ac2e5e17ebfb129301aa3d86f2586065f4a3c6e4a3dbafcd8addcf3c5293b`  
		Last Modified: Tue, 26 Aug 2025 18:04:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:35deb2f4e84695c0553518ffec8fb46c0da62358947d2ff36c4950764a20b1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eddddb932d77948adb6fb753ff30925ae4f11d28d8ac24192fa07b5d0bec13`

```dockerfile
```

-	Layers:
	-	`sha256:259488a0908079e202da03f96cadeed7b7ff7989b96f593707a39c6aa0fcb3eb`  
		Last Modified: Tue, 26 Aug 2025 18:39:59 GMT  
		Size: 7.4 MB (7378639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c09e91f345d2ebbc1924f7d901743e74bb1dae82dca836e8513d40b10b1fe2fd`  
		Last Modified: Tue, 26 Aug 2025 18:40:00 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:765e9875a2a836873907edaa350a7398dde2a5904f3a7c75a8554ca882c3b7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274131890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38188fbb9f7b990d2ed566dbdc98a14b303bd930cf4cb4f776e06623c260f2a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c854f0bb2062cb8e3203dbffc406ec501de420643779bca54d79fdb8235d74`  
		Last Modified: Tue, 02 Sep 2025 03:34:47 GMT  
		Size: 147.0 MB (147026994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f77b0a97b6eff2c185af919c492f2c6c8fb346faee6eeb4ccf59dedc16fe4f`  
		Last Modified: Tue, 02 Sep 2025 02:15:16 GMT  
		Size: 80.0 MB (79953989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6e0368cf551cfcf7881e9a252d8f9f3ffc8f20d98c6273a8b818756bfcc40`  
		Last Modified: Tue, 02 Sep 2025 02:15:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c314b6be9e9c4833ab08f37b8fc0e7fa429db403c66e42ec133a2004e786147`  
		Last Modified: Tue, 02 Sep 2025 02:15:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:1639dbf0110dda94ea24f30fb5197f6326d6ab6e3c49931ee181f59e76702c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a15874f38090797fa3ad1de608a6b5e25738c94e5620d2fecf971c7db06d6c`

```dockerfile
```

-	Layers:
	-	`sha256:91239a485da2ca81b3dc7eaf6e5fd35c3ff625cc14d5a788e0df93cbaacaef0d`  
		Last Modified: Tue, 02 Sep 2025 03:41:07 GMT  
		Size: 7.4 MB (7364718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b4769e83fa9f8bf6a439b82508e3de473ac556953820093756febcd3c4c973e`  
		Last Modified: Tue, 02 Sep 2025 03:41:08 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
