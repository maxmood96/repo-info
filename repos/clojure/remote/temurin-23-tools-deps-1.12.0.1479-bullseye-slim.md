## `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:018e852f84e72a7d1932147b96a2b61c10af7fdd4277ed1cf1777526af40372d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7fc9f3d0030062e11e67cc8129fbe0e8cb09502b56ab863f875c2bacc395d819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255637371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec035d3368e17e911ffa56173766740fbdaec74aa7d1015a3755eba880351fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79012ff928e60e39df52b7c64c9501df5710086be94812dc9a25f5e5b5b94a1`  
		Last Modified: Thu, 03 Oct 2024 19:00:53 GMT  
		Size: 165.3 MB (165267595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1738906a5d4c7579e761bb903c960add737692fa73e718a49d7215e0a0aade`  
		Last Modified: Thu, 03 Oct 2024 19:00:51 GMT  
		Size: 58.9 MB (58940140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec55e68cc14378bfe619c13f3724e0d85b84c87278048b314aa3df1a220ad475`  
		Last Modified: Thu, 03 Oct 2024 19:00:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7ad3dc092cba1d5f12a6c527fbdcb9a7d60a2f4f86a6c73b03cd813b5ae02e`  
		Last Modified: Thu, 03 Oct 2024 19:00:50 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd9ce4e0e4e631a018884c53c41f158536192d3deb0463149f07eb95669b35cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a14a8efb7aa6e62d085a59b50c51d8c17846b1a96413edc5389353ca10564b8`

```dockerfile
```

-	Layers:
	-	`sha256:e523990b7bbdec448196c8e94c10886aff75a5b828d871a38b5cfbc8e74c0f54`  
		Last Modified: Thu, 03 Oct 2024 19:00:50 GMT  
		Size: 5.1 MB (5104478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33926dfb2ce75158793ed355f86627159e271cc1640be24c603f0766781e5723`  
		Last Modified: Thu, 03 Oct 2024 19:00:50 GMT  
		Size: 15.5 KB (15518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aadaf376df0c219606e409b45aa65ed24c01c610e6ae91851b8b6b2e61521006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252402311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd79517f8dffe3a2f1f76864c8cda4fac1d3b4cfd808b82bf520353d607d5f53`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9ac7463badfe9cd4e79382a7483a7e964089c0caa19d9879a9181efd22d282`  
		Last Modified: Thu, 03 Oct 2024 19:04:16 GMT  
		Size: 163.3 MB (163252793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122974ad6720a09daeeb397402cb6be62445944bca2e6ee20583d1bf3d5c1478`  
		Last Modified: Thu, 03 Oct 2024 19:09:38 GMT  
		Size: 59.1 MB (59073321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca6f3b3e4daa9b59e5a07ecd8248d2bcc7cbfbce3ca46b96bea2f36a349d1ed`  
		Last Modified: Thu, 03 Oct 2024 19:09:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f9bf5fd83d414a89dea13dff1e8cb75c6c988e8817f0f234c6f888e60c78fe`  
		Last Modified: Thu, 03 Oct 2024 19:09:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:353d2251c841fe758318fabf2dca4254e9afdf1585ae98771f7e79db7a8f4acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7bda4477ea21c71696230a1690e26d379b0cdba5e5c91c82301188cfc7e017`

```dockerfile
```

-	Layers:
	-	`sha256:fa176a881a4d0a7996e67bb23dcf7c38a9a9904c242ca10bd5707dec9a60bee5`  
		Last Modified: Thu, 03 Oct 2024 19:09:37 GMT  
		Size: 5.1 MB (5109593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0cd58d50ddd9a5346814607b007aa037814e627924125a44f8c2fa8e626e95`  
		Last Modified: Thu, 03 Oct 2024 19:09:36 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json
