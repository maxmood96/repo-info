## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:64f879d4473d3a9cef52bbb50ecc870ea72a4cd1610be4b982041107b7492619
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1e31e3b0a93daea0698917c806f8fd0abeda42bcc4d79038a885d41ea1045b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175485165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9a0823a3d3340e06bf55786ee56cde61332d4f96b311226234202eb1b73233`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:14:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:14:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:14:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:14:25 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:14:25 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:14:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:14:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:14:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ed33c3c20abc7a3350886f7ea458a23e6d6e06fbda483ec370a9c19e559c2a`  
		Last Modified: Wed, 24 Jun 2026 02:15:04 GMT  
		Size: 55.2 MB (55198700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd73721b690841da8ffcad59195ed345c4e41a1e8a83159dcfe3223c21b103c`  
		Last Modified: Wed, 24 Jun 2026 02:15:06 GMT  
		Size: 66.5 MB (66512810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a4b24dd2aa83a185426040e517ed3eac169b0288b25d14d452f63f83170b4c`  
		Last Modified: Wed, 24 Jun 2026 02:15:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:19cea0daa08c8737838f674b3eaba7393cd0d309da4a4fb14a5e33611669a58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7540157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec55c071186ad912095cb67178d388c3008a28bd45827a0aad6df41d69f6133`

```dockerfile
```

-	Layers:
	-	`sha256:89445061c2047448c63c8ffa1739b33f22b6c3ed6254741f228cf40f8c8fa2e0`  
		Last Modified: Wed, 24 Jun 2026 02:15:02 GMT  
		Size: 7.5 MB (7525809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7764c03c8361db9465d22286948c5ec2c168f593b7dd46dc4fd7e6ee057221c5`  
		Last Modified: Wed, 24 Jun 2026 02:15:02 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:91cc3906a0984015f3aaa0c68b3bb64487205cbab51155de2b5a8a82aebb99b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173208756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71f297f2a1f65f4f618c61b00c4e900fe210c27f31f2fe24b1b63a42d6eb312`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:21:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:06 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:21:06 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:21:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:21:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0bace18025d9dd7dbc9b0b07a2ad6594ce6552db0d50c06679330fb4a0203f`  
		Last Modified: Wed, 24 Jun 2026 02:21:38 GMT  
		Size: 54.3 MB (54272901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e08ee2efaad2d8e5fcd21491e6b56eb797093aaab5a3a1dfd160a65d79501`  
		Last Modified: Wed, 24 Jun 2026 02:21:38 GMT  
		Size: 66.7 MB (66677991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626edad45a95674bcba456ebc0b3890eceac202d00bad4fb4b0b2c3c0b130e9c`  
		Last Modified: Wed, 24 Jun 2026 02:21:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d3d3b3a72bcfb3dce0ea92f94b6ae1bfe5fa46b300bad755d5cfcb68c645b4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc190e2c28eebeb30af043cca70bca345c3eeb10237fdf8137b779f9b37d2847`

```dockerfile
```

-	Layers:
	-	`sha256:5d3e94ee759a0edde8ddb97b395babb80f9174a554ebb51a9999be983bff40c4`  
		Last Modified: Wed, 24 Jun 2026 02:21:35 GMT  
		Size: 7.5 MB (7531608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d323d77e0e5edbf92fa1a874a8ca03570495759eb7b5be3db35e5ae8168bd6a7`  
		Last Modified: Wed, 24 Jun 2026 02:21:35 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json
