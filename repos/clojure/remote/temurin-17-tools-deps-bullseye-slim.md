## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:9c2119be4b30890b0c34a480cb547a6ad4b230aeecb5296193df01fbc9a48fb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:80799555cb366ff32c5d454ed0dbaed367eb22849a6654be3d4fe35e0903c4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235351151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4520a23b9d8b98807239db3f2fa0409dbb60acf4b7fa2fde3aefb4fb7c921c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:17:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:17:21 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:17:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:17:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e2b5a7b7b7d77953ceea2be2795907305ffdabd1727a76993fe31443b2a6f2`  
		Last Modified: Fri, 08 May 2026 20:17:58 GMT  
		Size: 145.9 MB (145905474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be02c87c5e86e112220b5adad0a1cfa256ae07c5e660d66d8df6e8f27a9016c`  
		Last Modified: Fri, 08 May 2026 20:17:56 GMT  
		Size: 59.2 MB (59186677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007de5ed34a88a619e73d7bdc7fb0fcb45d6b44a3d8f9e600cd0e0c222526d39`  
		Last Modified: Fri, 08 May 2026 20:17:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9613a7295e2ceedc6f2dac3279c4aec3098edaaec25a3beeea207a8eaf18b1ac`  
		Last Modified: Fri, 08 May 2026 20:17:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e586d5f1c8acaa15fcbf74513b822233b4de5bedd578e14a5c829dd722765705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4c2c177e21867caa35a71dcdcf5b7fcb22854fb13f5449298bff386ddeefdb`

```dockerfile
```

-	Layers:
	-	`sha256:10c189fb51a297b34908130eb85039cc8d9a57852f4b5fd1227641411247961c`  
		Last Modified: Fri, 08 May 2026 20:17:53 GMT  
		Size: 5.3 MB (5320680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d11d12e9cee49344a1552261a62b3a8821b7abd96c91c1d533e8b34bd6804f`  
		Last Modified: Fri, 08 May 2026 20:17:52 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b10c97d1edf1b8f12bb4ca8eebc261304105e9af750b1c941e38c0f20199b311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232798947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdb61b32c9453c596742cb5f56ebf8b71f0e67fbb24f07648a0b04c6fc0f512`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:21:31 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:21:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:21:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:44 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6da0c918c833f0ca01dcb50f1c4b79fd558adbff863900ddf2ba029c5ca8687`  
		Last Modified: Fri, 08 May 2026 20:22:06 GMT  
		Size: 144.7 MB (144724305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc98915b4133085a51425fd7380467533b116ec47b3e8da82ba856331ad67ea5`  
		Last Modified: Fri, 08 May 2026 20:22:04 GMT  
		Size: 59.3 MB (59331012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b0ccdfd7ed02dab8d788a767e36c21a6628023567227b9b4a152045ef91892`  
		Last Modified: Fri, 08 May 2026 20:22:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d0771fd8386b08d3b47d9e6bd869340c6287442a54941527c1b957216bd5a5`  
		Last Modified: Fri, 08 May 2026 20:22:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4e685c19d067d6f871d91c38eabcc3726b2aa065e0cf8da42ab1175044f7c776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c784ad7935aebb3fda0a81569c85f5e193166dad868349922369f9f02f44ab`

```dockerfile
```

-	Layers:
	-	`sha256:6217629ac82af545f028263e9c5a12c665aca9b76b1c5a41ec689b0def8cf043`  
		Last Modified: Fri, 08 May 2026 20:22:02 GMT  
		Size: 5.3 MB (5326412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b12d12d1ddaef6ed6f1135f2b4b9283b3f8f2bec92500c6c59dcac0da7a4c51`  
		Last Modified: Fri, 08 May 2026 20:22:01 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
