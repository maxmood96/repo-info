## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:f65b53960f6988b697880d98bf8d1d2c69c978840e3002fa538ddd4eb5c3cc4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ab30d83a9af493f776ffc31c38ef37082d60ff5e6e824522594c69d446e77f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234727529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87863dba52a7b3ce21a076f7f91ee0bce8eb28c7a6b3b257196e5c4f3569b041`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b8640f6842954e6b24865a101b7932c15c1c539a93042c0ac60da47fb4c551`  
		Last Modified: Tue, 12 Nov 2024 02:24:22 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6068d4425d17eea2e05f886fcfe55943c07ab989bcaa4093af56792bec2b87`  
		Last Modified: Tue, 12 Nov 2024 02:24:21 GMT  
		Size: 58.7 MB (58740168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e774488dd10998269dee4f17fa2d0e641ce3ba769dc4b42a8d6bed56d4fb9b`  
		Last Modified: Tue, 12 Nov 2024 02:24:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f1533028777e82cec45591ae56080481b9c29b73ca69ac1a3413692f8719f5`  
		Last Modified: Tue, 12 Nov 2024 02:24:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5442794698018783053e4c089167de8218a599afd0d4bad052f066d20bd80903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53b55ba58ef0dce11253960ffd85fb9cb336860f12484a389ad232b1050c318`

```dockerfile
```

-	Layers:
	-	`sha256:7d4e41a9e6cbbc452a6027a8f9587b3b2458c8d668fc082b903328e17930d61b`  
		Last Modified: Tue, 12 Nov 2024 02:24:19 GMT  
		Size: 5.1 MB (5125352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013aaf07013a3a13cdaae738da690f5f7f8a46b5850927ad4f47c6d2c9cc7aab`  
		Last Modified: Tue, 12 Nov 2024 02:24:18 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eeb9f364a3824b249fc1ca5b2d1868edb72e9a73bfa29f8c98067732c1582a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232331295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8808f118e54cc4268f879ffd9422f156151f33c1bad6037a10204153566000`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31953610c7b09ebf0d81c48ba49aac2b551349dd325a1cf13002226875a5a2f8`  
		Last Modified: Wed, 13 Nov 2024 01:24:26 GMT  
		Size: 58.9 MB (58877683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef07f3130cbccbdcc4511a36b3e9ac5c704aee8e9ece308281ba498be6c65669`  
		Last Modified: Wed, 13 Nov 2024 01:24:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1d7fc4eca692ab171431a46e78602ff6c32564eedf1c0c10163c84cdb1abd9`  
		Last Modified: Wed, 13 Nov 2024 01:24:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8c2b9c49cab57f2b9cf626dca5aad3dc84d29502774d77db7adeee52b197e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c5cf72481608148e1d1f5e8277c8f8fdea9a7fd1da715b7d4bf26f97935faa`

```dockerfile
```

-	Layers:
	-	`sha256:f32b898ab75cb2f68199394c8902322cfd6eb6314f826277f58ed68a08868caa`  
		Last Modified: Wed, 13 Nov 2024 01:24:24 GMT  
		Size: 5.1 MB (5131089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce61a62a8a7eefaed466ca6b905280201bb492d2391ec2b97e040524c270df9b`  
		Last Modified: Wed, 13 Nov 2024 01:24:24 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
