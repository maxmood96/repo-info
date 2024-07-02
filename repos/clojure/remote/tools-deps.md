## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:8525c985fc1516a26fa2f5e5b0f2d9747fa243513313b398280c9481c7a6db88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:c69b8755f616060a2b94145f6434a80810cd091df2709561dbcea86383874b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288565302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0a62962de7088d2de817b70b819d8d36e911df11907299e7b4020f213bd200`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020be607ade0799a12cc7a764d351a663b12e39aa336e23be38b432ba77a721e`  
		Last Modified: Tue, 02 Jul 2024 07:07:10 GMT  
		Size: 158.5 MB (158497952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e38fc4b0ee1f48d431bc73fdce89f677bd743536306e5f8a441c3a4494183b9`  
		Last Modified: Tue, 02 Jul 2024 07:07:15 GMT  
		Size: 80.5 MB (80512248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0e317a0636ce032ae280bf0744574316ffb5fc4c2f3f54be7a41fe6a0ad9be`  
		Last Modified: Tue, 02 Jul 2024 07:07:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496705daf8b03f1821c5f19274b421aa203803a0bcfe5884f499861a49410d9c`  
		Last Modified: Tue, 02 Jul 2024 07:07:14 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:edaa5d0e0ca25cfbb223b859006ac801bd147c6ca7711573f9e6c6dda7155826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6979410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f8986c415b2b178a3b7be72b46547460b314fa801a45f44c90375490579706`

```dockerfile
```

-	Layers:
	-	`sha256:b536e3f2462a56078a7293f14e895882b7f94e612f8545cea0dbe8119722ce27`  
		Last Modified: Tue, 02 Jul 2024 07:07:14 GMT  
		Size: 7.0 MB (6961971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b25d1072b3c20b40c918736e2ae6c705892323b5053123ae09bca4e03c13d6`  
		Last Modified: Tue, 02 Jul 2024 07:07:14 GMT  
		Size: 17.4 KB (17439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd429ba9b09555a5c142bbb49ae058fb72f94ebcf4f7001486588297783694d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286517323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b99d6754015e7387255cdd7457f7b54abdd42d417ed947566685b13d0d63633`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e62d15ac1abd044e9ffb7336f4a9b7325c5f14fb2a35239455ac5a4c6bf166`  
		Last Modified: Tue, 02 Jul 2024 09:10:13 GMT  
		Size: 156.7 MB (156665591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be115f946541c44bacc4f2d443af3b9ed10240e2b5aac6cffca93ae28c299d3f`  
		Last Modified: Tue, 02 Jul 2024 09:39:43 GMT  
		Size: 80.3 MB (80262242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ea128e4aa3f7ec6d260151f78386f8f11db68e670501067e931f664f390ce5`  
		Last Modified: Tue, 02 Jul 2024 09:39:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51c0038861d8bf9877dbc337d1ea6942f7485b95b554e6ed73a101dd4f4b15b`  
		Last Modified: Tue, 02 Jul 2024 09:39:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:b54b1aa8b0c4923cb3e99a4d02ed40ee4db85e1d981ce6a9f7c805daec877f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6986477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fe860ac81c282c41e9827f3e0083be3a3bdd2992043c8608d1e9b707d88aed`

```dockerfile
```

-	Layers:
	-	`sha256:82bb9bc730a588d040abcf16e49fcccca8de1d0a4a0e8bf93c151d43d03f63fe`  
		Last Modified: Tue, 02 Jul 2024 09:39:41 GMT  
		Size: 7.0 MB (6968430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c3a4b1b30e555a33e0b22f7eb3181003f87143ad771b7a83e8b2f997525c1d`  
		Last Modified: Tue, 02 Jul 2024 09:39:41 GMT  
		Size: 18.0 KB (18047 bytes)  
		MIME: application/vnd.in-toto+json
