## `clojure:tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:309a43343870fc0ca6fc7236e1d7783537ef5968fc871eb7abfe9c8902033943
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f2300519c7f315a57f70d16ef4d11f2b635820dd830363b47aa4db3f838bdb46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182019895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f968327383d37cea2f1df87bc9ecbb24bd3913d11f6de8f2a84d4c2c813805`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:19:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:19:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402518d0bd570ce4493c950dd1633098128e4952cadb4641058678964f8141e0`  
		Last Modified: Fri, 08 May 2026 20:19:59 GMT  
		Size: 92.6 MB (92574587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ae63676f11b3ace34779b942f6a69665b8409a99a37e60c933f665e3b9b655`  
		Last Modified: Fri, 08 May 2026 20:19:58 GMT  
		Size: 59.2 MB (59186308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a205b0d18df42410da1aac9750dad58c814cdc9384f537b4d26cff58d851edf6`  
		Last Modified: Fri, 08 May 2026 20:19:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671bd2d80735c5e20d81f833684490a48a56ba2191d3ad13f2e8a3515ce59e6f`  
		Last Modified: Fri, 08 May 2026 20:19:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6475594e6e3d3e4ea5d7d88a15ddc7c8ea199b0f2dad25569b38530fc7d3525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424cd0fd23eb74d73c4511a666f59628ebc4f820ab3cd3d21ca3072eca65f05b`

```dockerfile
```

-	Layers:
	-	`sha256:aec6c73d38880b09fff505e35e7ed8b83663644d3eac287e21a915cb4a8ca148`  
		Last Modified: Fri, 08 May 2026 20:19:56 GMT  
		Size: 5.3 MB (5288770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca7d81b2784fb316c14e1019a2f30bd6fd07877eef75bb78d7629709359a8f4`  
		Last Modified: Fri, 08 May 2026 20:19:56 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cd61a0c10c2a9071507e53c15c0a9d303822b8d323b979eda417d8d310f9ac41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179617044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057fb9a0402498963e237a56b6cc168f197fe94deafb8e66935d26b10b6bcdf0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:23:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:23:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:23:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:23:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:23:51 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:24:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:24:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:24:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:24:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd30a660f28416f8a0bc17a26769597cfba0b22f143659fa1523d91c66fe223`  
		Last Modified: Fri, 08 May 2026 20:24:27 GMT  
		Size: 91.5 MB (91542269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa33da1fe3516975a5332a71921a4d68a842af7f17ff709a58fe29b5aaeebfe7`  
		Last Modified: Fri, 08 May 2026 20:24:26 GMT  
		Size: 59.3 MB (59331142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2af8968d367cb9468cff26f39ac4901ae3e32fd746ef72bcd72f34dd796a05`  
		Last Modified: Fri, 08 May 2026 20:24:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2f325d626747dd04c5bba0ecd3eab6fca2c69b1d76c8a8cffd70616ecbe539`  
		Last Modified: Fri, 08 May 2026 20:24:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93b9a419e5416fdbd719f63f9327cb6053f6f3eb4ad4e720d6c580fceb1ba533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4601c4e2ae3f60462a6293c4723eb576dd06c717f51e883cd04c11ab057d1519`

```dockerfile
```

-	Layers:
	-	`sha256:de46fcceae5d5f849e67115afe4f867ef1328d17d2d68426ca01be6b74872ced`  
		Last Modified: Fri, 08 May 2026 20:24:23 GMT  
		Size: 5.3 MB (5294523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7512972808d0bd0fb0b45c58c71edf20d01b8e98876d7637c27f3bdb5fb2cca7`  
		Last Modified: Fri, 08 May 2026 20:24:22 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json
