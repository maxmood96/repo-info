## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:a11a0969e34b123968f0033c5f012c8d56718470d6839262e9045e3492e31851
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:53d4d81bcdafb4a481f4aebf7747981cd9adeee3459ea86ca9f96e453156d91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235069191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e42cc2ec8be0894a4a305f39a63122b4cc1ea2ff1dd29fcb4702ae95799bc75`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550d7752f2a818247c01abbf1682326d16a42e78652093bbb2dbdfd03afe0481`  
		Last Modified: Fri, 10 Oct 2025 18:50:40 GMT  
		Size: 145.7 MB (145658349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d310ce0c93c0d4269b779838fe2c84922d570f1e8cc95b4712c1b4f9efa768`  
		Last Modified: Fri, 10 Oct 2025 18:50:27 GMT  
		Size: 59.2 MB (59151834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7f4ec660de46efd4b0cd4e74db1478cbfa78c3c3b896e0cccddc8318ff938f`  
		Last Modified: Thu, 09 Oct 2025 22:27:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:604b73d78e3986fa08b589866ec1f7cef383bbcc34e136a24856c377203e6fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5344142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60e8ae96be160bf6062738c853c8484fecb5046296db71906760a470c70b00b`

```dockerfile
```

-	Layers:
	-	`sha256:ed2c397b59949c86dd460447e1ab520099ba9000af6358bb3bcaeb1fd1198fcc`  
		Last Modified: Fri, 10 Oct 2025 06:36:34 GMT  
		Size: 5.3 MB (5329832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97cc19d95b4ffbf811e1308ae553f81e4fa40262009f2b787e19cc897e5e3750`  
		Last Modified: Fri, 10 Oct 2025 06:36:35 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:825378315865672aac8c673bb860f4f54cb819e5ef3b28ec38e97cd9e26f3926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230497412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3084a178f405f92ea46d5c36de91533467957ffcdacd510d46f8f74606304b4`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6549c7ec0673609216bc978a2ce19d5ef51a2a139b4f776c1c92080c346cd6`  
		Last Modified: Sat, 11 Oct 2025 04:29:02 GMT  
		Size: 142.5 MB (142460659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e47dc05579e91809fdbd738154f6ee82e42ab3643c2e83883015ead23234a1e`  
		Last Modified: Thu, 09 Oct 2025 22:27:40 GMT  
		Size: 59.3 MB (59287679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b1a67ffdebf9f67ba2b7fcbec7cb84dc0e0481262d7adbe0ef5f36a68ce1f5`  
		Last Modified: Thu, 09 Oct 2025 22:27:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d526dcb7c93afb09c9c72ad02240a6f5b900618f2a89bdfc04a89153e9695716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a018981c5cf96ee3535ec1dc633da35fb87109f0ce1cf1916fb232e47f269d`

```dockerfile
```

-	Layers:
	-	`sha256:70dfeb6ce5efff2f3fea5aecb24fa627a0c9f7df4d07da0892ac1700309d4cbb`  
		Last Modified: Fri, 10 Oct 2025 06:36:39 GMT  
		Size: 5.3 MB (5336182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445d444c348e94979dacb7198fa8da3a05db5c0e9305152e35546208d2760288`  
		Last Modified: Fri, 10 Oct 2025 06:36:40 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
