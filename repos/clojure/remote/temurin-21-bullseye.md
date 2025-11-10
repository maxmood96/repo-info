## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:e45d4f7612f65eabf6628bb880a8fb1bbbb51fdeef31c8ca39f41a9db4a275d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7a9e9b780a3460d7ed12e6365d95de39a8d695118682ad68290910d1bf831861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281144527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612fb3b82069b8c63020491edd7419aff82bc66907788ca5f20d97d779aa004e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:44:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:56 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:56 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:10 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2833ede422c52f57fcc0a0c33e3ba000bf4ca4db4a715435942f91fc3819b3`  
		Last Modified: Sat, 08 Nov 2025 23:04:16 GMT  
		Size: 157.8 MB (157825975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b774b91de858b04e1764c5da385b20e0004ac314bce6753ff858a557c3bd3e`  
		Last Modified: Sat, 08 Nov 2025 18:45:53 GMT  
		Size: 69.6 MB (69560813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51650a7ef35a8d20c64f0d5a47980ce13c207a99bd633e9827d4f83aba87cc06`  
		Last Modified: Sat, 08 Nov 2025 18:45:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff74c6af976395f7962f653b61503bd3ff9f0be07acde978dd3bc3fa066f4b`  
		Last Modified: Sat, 08 Nov 2025 18:45:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6a38911ff571460cf8973e8301b5079357dc82eeb8e41a868889bb08dcdde750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39029b5a5c80ecf65ddeaba388138b58bb3f7206b417d5c765e147985c0907e9`

```dockerfile
```

-	Layers:
	-	`sha256:864a2701f6de4d330e71c05483dd9de47abd5f01f461f538a7ed296999db35d0`  
		Last Modified: Sat, 08 Nov 2025 22:46:18 GMT  
		Size: 7.4 MB (7398771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716127e81ba434be45f661e4b0b5063952dde9a0edab1b2d0e2a5c4fe4863c3a`  
		Last Modified: Sat, 08 Nov 2025 22:46:19 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3643eb4c413a0f441a6336c42bb6c65883c5c41d426ec8880007bfbc688fdcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278054852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac77600dee4405400347b86a41317f7286ef727987d8c41893d958f735c46ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:20 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:44:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:44:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:33 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db1c132d3d9e577fbb5ae618177df1f6a3410e87628490f7540adc0ec5603d9`  
		Last Modified: Mon, 10 Nov 2025 03:57:42 GMT  
		Size: 156.1 MB (156107621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f4f1a58539586e3f12cad73ba4d5aaf4c4e4ae80b636fa6beef120d1509d1`  
		Last Modified: Sat, 08 Nov 2025 18:45:28 GMT  
		Size: 69.7 MB (69688218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4fbfb0afb5c38598113a4aaa5180c0b05cd98544acf18244181f136005966a`  
		Last Modified: Sat, 08 Nov 2025 18:45:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3633a7598e96df078c877abc54578c1fa9cc10f6154195b38d93a10950628f3`  
		Last Modified: Sat, 08 Nov 2025 18:45:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:47c91bf7e15ee0b976e4342be3f8d6035a3e8fdf5414b2b8cd43457cb59d6784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51ca82c4383b41f0f7128c59fe171ad892f63028ed36bdc4d73888940cb4a6b`

```dockerfile
```

-	Layers:
	-	`sha256:914365cb147ae8f2876e34d30c657c79420ba16ec659c578c8c311936e0332ae`  
		Last Modified: Sat, 08 Nov 2025 22:46:25 GMT  
		Size: 7.4 MB (7403870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c0aeb5253f54cfead611ba198ac0f7b9c1ad2d58df3c7300d0a767b9887b8e`  
		Last Modified: Sat, 08 Nov 2025 22:46:26 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
