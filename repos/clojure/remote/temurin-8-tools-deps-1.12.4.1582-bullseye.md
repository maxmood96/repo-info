## `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye`

```console
$ docker pull clojure@sha256:5d314a00d38bb10c53e7364ba4771a3b068f36b3c4d193a35ed8752024cf140d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b0582b6fd6f24841425ace221a97d314136a44a969630e2e71b7fc40d2521836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178047276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8624bf80686390be9ddb51a21ecedd5986cba6efabcdf1e557d3b4fa2057dc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:44:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:44:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:44:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:44:23 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:44:23 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:44:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:44:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:44:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc87ad53d0cd8ff984bbfbffb7ce42080bd5c93231374e5898d284e1626e12e5`  
		Last Modified: Fri, 16 Jan 2026 01:45:23 GMT  
		Size: 54.7 MB (54733362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ff7bc2f072225da320132498e8bf7cdb394c4b2a4bbc9d1f315dfb4b515f1`  
		Last Modified: Fri, 16 Jan 2026 01:45:06 GMT  
		Size: 69.6 MB (69556821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529fc99c5f0a7259936f4672dfad65530ac29f37c322436b5ae659c50c091451`  
		Last Modified: Fri, 16 Jan 2026 01:44:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8dde55a1e9ed5adcc70b35489e1939ab8441286bd9e893ccc58edab0e562c7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d907095d6dc98cff82229f876aa8cb47a20b81ce3363a0cb932478393a255a2`

```dockerfile
```

-	Layers:
	-	`sha256:577db7c61a91a112ed5d9d9fbaa55a9f92790956772dcd2f4200190125363e49`  
		Last Modified: Fri, 16 Jan 2026 04:52:22 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4d371e2e408bc98a976f2648ac6cbd94361c216e122481bcd59205787149ce`  
		Last Modified: Fri, 16 Jan 2026 04:52:23 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fd56e1d1b172d5d93128ce71d31f8244debb1ab993d9021ec52b2f3f81419e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175760464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9ad64383b46daac5d44e082f93da4de932493b6c17cec73aabab759579f2bb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:48:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:48:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:48:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:48:09 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:48:09 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:48:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:48:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:48:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89cf26c36d39ab85ed01a04a880d9b1dc62f716fffc5a0109604b0580a0233c`  
		Last Modified: Fri, 16 Jan 2026 01:48:41 GMT  
		Size: 53.8 MB (53815012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90c8611ff6f23e70152230cc01190bdb650a82527729c73580ee2bbd25f1254`  
		Last Modified: Fri, 16 Jan 2026 01:48:41 GMT  
		Size: 69.7 MB (69687037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e2be66e81ea75fd4750682f7db0e2d7ae0bc583201344cdef816087c7ad3bb`  
		Last Modified: Fri, 16 Jan 2026 01:48:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e526eccee3834b32bcddc93b164d4f69e94e0c008cb909cab5e745fa83c0c57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbf47fee76e576d4cc3205e82890dc43e2579b78a2b12acbecf3f7778e463c5`

```dockerfile
```

-	Layers:
	-	`sha256:cd5776417a04f473c6c57538ebdfd50969dfa0349e5d91583a54143dc4738c51`  
		Last Modified: Fri, 16 Jan 2026 01:48:39 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95806f2b30379e65d4f6bcb5098aca336af96a7bc15efd5174feb82d8f7302a6`  
		Last Modified: Fri, 16 Jan 2026 04:52:30 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
