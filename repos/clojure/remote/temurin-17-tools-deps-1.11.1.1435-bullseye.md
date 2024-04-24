## `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye`

```console
$ docker pull clojure@sha256:ae999345200047e718262d4caa40580cf199603d61b8af749bee0e075ac2462e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:58ce3ddfa5c0f1552067b6b70c1135a4305a270897510ae7129d02b080cd1710
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269212210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df273c1bb87a1138dfba4ad32e0c59c52affb9117b0ae1e11efe9b7f63b05b5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:25:10 GMT
COPY dir:61bea833528044db01491107d8c3fb583322243082c7798fd60ade98f7eb7613 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:25:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:27:36 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:27:36 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:27:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:27:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:27:54 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:27:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:27:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c9e51bdaa7057a201c425de35327e310245347152bd3336f67a330587e7052`  
		Last Modified: Wed, 24 Apr 2024 21:48:40 GMT  
		Size: 145.1 MB (145095326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84967ce9f339b7424a4fc608c8676e8c848a5682a302bcddcb9cd13d2664e63a`  
		Last Modified: Wed, 24 Apr 2024 21:50:28 GMT  
		Size: 69.0 MB (69016998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fc6668dd6298454b083207c53fdec6ce185f6760e59a6d855bf0be10f8707c`  
		Last Modified: Wed, 24 Apr 2024 21:50:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34daa684f2c04e306f1fa78b5be0009df4a7688a6e115b7a2e2a11ea6c0f5889`  
		Last Modified: Wed, 24 Apr 2024 21:50:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ceb0c8542f92c7ecebe059a50014f23d3abc4c9449c5ce9189f976be55d9c7e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266775007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b98bd0dc626b60eea75caf8b17f6fd45a8cc2606f842dc6603796ffa6a84cde`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:09:33 GMT
COPY dir:894420f494a8d73ff0a7e5986ef0142218654b95343c81b2b9fc9a9d3ea0c174 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:09:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:11:35 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:11:35 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:11:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:11:50 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:11:50 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:11:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:11:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839c73783a4977552a7c0d1389763d3ff68da6020dc9345ff6ab8071d145d9e4`  
		Last Modified: Wed, 24 Apr 2024 19:28:51 GMT  
		Size: 143.9 MB (143891816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0465be57e273381195ab2b7916e9322a0bd6b3d7868bd737272976f3c8309307`  
		Last Modified: Wed, 24 Apr 2024 19:30:26 GMT  
		Size: 69.1 MB (69142213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f256a403570d6fb1179aea47c8b763537e7cc8118c34c646e61dfefe2e8d151`  
		Last Modified: Wed, 24 Apr 2024 19:30:18 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d170e5b5ef9cd5429ee1589536c444f6118fe5c635097dc3b705fd779f30722`  
		Last Modified: Wed, 24 Apr 2024 19:30:18 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
