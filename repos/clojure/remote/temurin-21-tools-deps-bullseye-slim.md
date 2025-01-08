## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:4ee6a0224edd3b43e48acb82d630312a062953292442b5bfdfbf7967292c1732
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7e918273561bf38ab1ac709deabfaa25ba8f2584aa4008ffa4e61560d4987820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246602544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8972689a62ad12f6e0125f032c6eed3e7b006c01fe66bfeb7196c1af6e4123a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Wed, 08 Jan 2025 02:30:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6f3ce05d1170b1e86863d3df8ac27e879de6fae5f86852b8f87f8ece61f728`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 157.6 MB (157568689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088107c42a36e656fb0faa92efd279f1c926d7177c9b43e84e792a0771473e7a`  
		Last Modified: Tue, 07 Jan 2025 02:29:32 GMT  
		Size: 58.8 MB (58780175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273cc6dc050f63b620ea842265adc6e1c786d5d984a1c64f6c24759df3525110`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed1f86d63e58969ecf8736ad617bc2f8ccaf577498c79422c8e276f23cfa9f8`  
		Last Modified: Wed, 08 Jan 2025 01:31:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:804b967c008cf7a5977cea387ee856d6ce0e77141f854f2024dedc30be49d204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c314d6059919bad74fbccfb4d1a0bf762804903c00d697c0c9088637b655a158`

```dockerfile
```

-	Layers:
	-	`sha256:e12aca2e3bd1f6ff34f0bb92849d627f491bd7823dbcaf0964eeb1f36c4ee586`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 5.1 MB (5120867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728be1617f89f4f7f1ec9b2e0bccfdf56b074e3b90fb10f699491e83dd2b6ca4`  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:103d0daebb625b4a7bc0bd6df14b799bcd97ae4db6c784a94b812944adacc6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243444177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3931701b93f7f50ce41603ccabbbffb77da6617ffd077a547456c9d48f553010`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416a3a2fd8cd9807260966b02586a95c093ce6d1bd3085e2276d72f97ddf05cb`  
		Last Modified: Wed, 25 Dec 2024 07:33:18 GMT  
		Size: 155.8 MB (155793154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507e7d736a8a13a2d9a49ebebffd14c83ee9ef03b8bd7b7dec5827ce4c6da41f`  
		Last Modified: Tue, 07 Jan 2025 03:33:49 GMT  
		Size: 58.9 MB (58905129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b6260e195928fc38cdb9e75b89fda2baf3771903469963fb93fbcab0fdccd7`  
		Last Modified: Tue, 07 Jan 2025 03:33:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd47f052b304cccc68cde06c9f6ec1bf0a0c55ad0c6b7f5be1cdd524dd213fa`  
		Last Modified: Tue, 07 Jan 2025 03:33:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:edb4e9e380039043b74148a92094147ab76965cb4a31fd43c3fcd9e6cf41c56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3aec82c02313e939825639e5031860e3b219051872014358321d4576aef98`

```dockerfile
```

-	Layers:
	-	`sha256:8cabcd7de38d8ad996b04162ee46a9d3d1843760eccc9e06642a65e0787fef1b`  
		Size: 5.1 MB (5126623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4651d1fbb5490cda49ecf8bc0ed060acc4077296bbf89fbda1069ff96e9c4ef3`  
		Last Modified: Tue, 07 Jan 2025 03:33:47 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
