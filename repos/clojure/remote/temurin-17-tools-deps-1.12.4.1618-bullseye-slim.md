## `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:9bb23b80c45e0db6b31bc42018c8757cba2fc0f60a853307528ebe00aa32a89e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:04083841b93f5ddea53ec69513775203f61c3be9f9dbe0fddf97b15e3041b3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235070842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de0d9f6c728484cff04cd7ea51e12d382adffe8e006b74e8d84ce93813be2ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:58:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:58:35 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:58:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:58:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:58:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:58:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:58:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcd00ca068cbc7aaf3f90c0c45249cf323a1750d52583b0db1719e19c6a5bd5`  
		Last Modified: Tue, 17 Mar 2026 02:59:12 GMT  
		Size: 145.6 MB (145628408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190e27a255d5ea60e5412a8b4e106fb08a59a84f2ab30c8b92c0358dc0570627`  
		Last Modified: Tue, 17 Mar 2026 02:59:10 GMT  
		Size: 59.2 MB (59183569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8860eb78593b60e5aff404b9c3dded75cb82b7d44d608f70cad23fab260607b`  
		Last Modified: Tue, 17 Mar 2026 02:59:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb73b452a399e01e47292855e73011335db455bc7ee64bd89949b9afaf55d4d3`  
		Last Modified: Tue, 17 Mar 2026 02:59:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:158d16291311dae9551ecb8afe121bcb5afc9fc50fed29e6d552d1d130aa3a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7db4cef5a39223db44b458294731e841fc01255d84cb2123bcb7761064d606f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e43f85b00fa161fad533de126ad26e375be7c497b57178f67bb2ce0a4e9973`  
		Last Modified: Tue, 17 Mar 2026 02:59:08 GMT  
		Size: 5.3 MB (5320053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03574a1541c38f5566fe0451e7e2256007607cffccf13f0e330f30b49978f8e4`  
		Last Modified: Tue, 17 Mar 2026 02:59:08 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ac67f94a73a9128ec6c8c4772b3c537ab9a4102d10007131146fe72d1ddf9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232505513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a3a2468393676678c966bf0870138fdfc14f409617f28b3703b1eee8db4334`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:03:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:03:14 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:03:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:03:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a4d3bc7722f1c3e83a386ac4aedd18dcca83793fb087605a33186a4589bc5`  
		Last Modified: Tue, 17 Mar 2026 03:03:50 GMT  
		Size: 144.4 MB (144436240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b13d5d9bb3d3ddb2bf6ab0e54a23b210b79654a1db579bd07500d7490e4e47`  
		Last Modified: Tue, 17 Mar 2026 03:03:49 GMT  
		Size: 59.3 MB (59323708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30246a1bc1b28374272b534149b50095c2fd61fa0bdc5150dd6e0967697e35b`  
		Last Modified: Tue, 17 Mar 2026 03:03:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c462817c8bca7e5847bdd96d1b960411c679bcb09129ffbe972bc057340906ed`  
		Last Modified: Tue, 17 Mar 2026 03:03:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8dfc35af763c66fa4d136a912ec529d40444f306f2c2942532da370243a2236f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8376364ee4d22c2b188403eac24e25ab30ff672277980479165565d1feb865e6`

```dockerfile
```

-	Layers:
	-	`sha256:d743933da5b2b1bd37d7ff09f5d635a708b7d7bf9e78a8821bd7f2364a55b150`  
		Last Modified: Tue, 17 Mar 2026 03:03:47 GMT  
		Size: 5.3 MB (5325785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cf5217f903726d18ec85b630848ec22623a884311172b2ddcd4b21dde1e245`  
		Last Modified: Tue, 17 Mar 2026 03:03:46 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
