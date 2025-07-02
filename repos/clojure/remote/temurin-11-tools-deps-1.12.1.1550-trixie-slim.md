## `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:4568c48990867914204482be949233f39403f29f7fd9c70d7c93f7ac6c5b5a9a
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:212b405ba095644eedaa3471eba455251da70d6d69640bd2d31f15b9531f302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247209173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7792ec884703b9a3877922154e6b1c8ff23f0504e08e77d10006e012a3417a`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171eb4b8e11a24f99208f462945890c8c5ebf06fddb1d2579ee8f0b9fa182b6f`  
		Last Modified: Wed, 02 Jul 2025 17:04:23 GMT  
		Size: 145.6 MB (145635731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a119c0c018c652758c944ab64c3225df69c007d7dbabac8cc531c4197117ca`  
		Last Modified: Wed, 02 Jul 2025 17:04:07 GMT  
		Size: 71.8 MB (71811690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e8de3bf350c7b4a4c067bc5fb315f0be63384bfffc890584cf3c4844c47f73`  
		Last Modified: Wed, 02 Jul 2025 17:04:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:15f6993b1b405c973cc5921467526653a358865d26a0e7f1d8519d190be6fb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1d10824c74ae6b8f48655f0a742472ab8e8dbba984bcc33628e3d8fe9a0d91`

```dockerfile
```

-	Layers:
	-	`sha256:6eb893eea47f19a731ff5aca87f50cce290e779d3c8430fbb75790a55fdd7406`  
		Last Modified: Wed, 02 Jul 2025 06:36:48 GMT  
		Size: 5.3 MB (5272943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa1467f38d2c83024fb808f17864543a63495ff945f91a86d12754e6258325c`  
		Last Modified: Wed, 02 Jul 2025 06:36:48 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25c960c512d8bcc32d4dc0a9cce801c9c8ccb2732968ffcffb532205a4a993ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244190936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3cdd89e274d543cdb6e0fb1cd69dff947c5959a1da5b350ac52fb7789a35a7`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9af3565728f2151458d03a9d2f8e348f10fbd83aa67b85dc0f9f6cec67054e`  
		Last Modified: Wed, 02 Jul 2025 17:05:17 GMT  
		Size: 142.4 MB (142420717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59450f430dc7e97819ece9eb2918289a48a8450dcc5ad0ba9a1d5542822a9f8`  
		Last Modified: Wed, 02 Jul 2025 12:28:31 GMT  
		Size: 71.6 MB (71642710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8920bdc0136d97eddc4928bbb60496528ff74a89de646f3999d2925eeb0d4d78`  
		Last Modified: Wed, 02 Jul 2025 12:28:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5992a96e6d3300e3466c45a9fa48de9555e150c56b368511d4321e09f61eaff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b002cf2d038f01d9e1929d612947802cb45b036f0873d2ff887c40bb75a5df99`

```dockerfile
```

-	Layers:
	-	`sha256:0d01a076a99d7249c22d5615b11ea0cf676cb180a8909c06a56571e5369b6e33`  
		Last Modified: Wed, 02 Jul 2025 15:36:51 GMT  
		Size: 5.3 MB (5279330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10d0ab22f69a607a818754be5bc1f896df674c600bf3b230aa81e2a7b16d9a4`  
		Last Modified: Wed, 02 Jul 2025 15:36:52 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c8d25a27387e1f43554e29b02c51df07b8526fbfa540649b041564c724427ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243630054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d2c1725a0b2316da2e55531e812e2a19297b1722e5b5f4da2e6ce1ca50ba1f`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676faca439b315e8d443d62b4f05302a0a6134f1d73456cdb753985d6bdcded9`  
		Last Modified: Wed, 02 Jul 2025 10:16:42 GMT  
		Size: 132.8 MB (132810428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a8db61290a8f425b32b0da7b6de3711f539ef84810e1450290d0905855031f`  
		Last Modified: Wed, 02 Jul 2025 10:24:52 GMT  
		Size: 77.2 MB (77232945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bf21a9f335e9185a9ccd1e78790c96ebe38457f9568378e0e73894436dda5f`  
		Last Modified: Wed, 02 Jul 2025 10:25:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ad15609cf5ce3e21e69fc4498a36888e0e396fa8c783ce475c4a403863c6efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6c28c809fa7e9c4025d5126e6c6a3a4c4a02a0ac40a9d7e6ad9403432d4c36`

```dockerfile
```

-	Layers:
	-	`sha256:a5fec05f6fd517664533b3e790e4c7b448a6c48a8c6fe0a771bbe560f4e56124`  
		Last Modified: Wed, 02 Jul 2025 12:36:35 GMT  
		Size: 5.3 MB (5276699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f496b6b7ae7775ec5a3e3370161e2c8e93064cc171793f8c6a62ab75ca3b74`  
		Last Modified: Wed, 02 Jul 2025 12:36:36 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:56e027580bdab734a8af691b276e4dac2c62008bf41b54640af9b91a2aeccca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228227465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d53ac2e1e00d772e1c917abcbb2419d64fb566305675eb9c6545d84c0f6079`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55851921fd048c276b34305ea0c927a8ec9f9a2fad9f3541c4844ea06218e4b`  
		Last Modified: Wed, 02 Jul 2025 06:28:56 GMT  
		Size: 125.6 MB (125586107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707e4f90769101c5aedeeecb3b11219792523130efc94f9aa7c547673c252265`  
		Last Modified: Wed, 02 Jul 2025 06:33:53 GMT  
		Size: 72.8 MB (72802368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ba88a77fdab6237b1921d8cc628c63ce77fe84663fcc1d99deaf752cc079da`  
		Last Modified: Wed, 02 Jul 2025 06:33:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ceec8fb87d90a32cc2bd37f552e732833ead094f56a191225b7babd021ffe456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4aadc57ec38cd7b0c9c7676d5fef56f1cf425aa0f52654c71dc6c3528b0a168`

```dockerfile
```

-	Layers:
	-	`sha256:d98198b6094d3a867796673caa4a3e7dfa326f01918fad00d45d347fe073869d`  
		Last Modified: Wed, 02 Jul 2025 09:36:31 GMT  
		Size: 5.3 MB (5268871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f24068616724f1474b6d94ce9ee2707e53af124e64f2d4781abd9d1059e3bc2e`  
		Last Modified: Wed, 02 Jul 2025 09:36:32 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
