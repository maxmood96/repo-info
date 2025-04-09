## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:9c2b96ace86d2bf30861e84ac344e4eb81ddd82ee61fe5942d697fdba9916c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:89d991c32f92295a565c48f469b6ae4fd85e1edfaf4c2fd1ea15149dfaed2ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267711122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c7d1423babb6c41417790ecc7f7a7970e4f8b7b04fa633440ec8b5b7467b93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a70ec081fbe5483487a649b2193a32f747c470c27017d713f7d66bffe2e87f7`  
		Last Modified: Wed, 09 Apr 2025 02:19:00 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05168e70ea5848c53b9c64561195fa0520c900df163b2ee4fa6e98b9dc414389`  
		Last Modified: Wed, 09 Apr 2025 02:18:59 GMT  
		Size: 69.4 MB (69395025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831a553bc64e65eb412f2d6443e3f265d24b34a40d0b8e3e32e9ebff7656e29b`  
		Last Modified: Wed, 09 Apr 2025 02:18:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6bf15979fa79dc9e4b693b2deebb7fb9c10b2b7ee31b5d29a9eb852f32a7b0`  
		Last Modified: Wed, 09 Apr 2025 02:18:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:327706a2447bb68371e7edb5e06ac178bd1e4e1e89af43156caa63395f9e8bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e315772660fe8f61aa53e74e95bbaac2b2199dbee3242f499564a67f0e279e9d`

```dockerfile
```

-	Layers:
	-	`sha256:08574b10e30ef8289cb53f06b4465364542aaf6864ff45dcc70894548a9f0e4b`  
		Last Modified: Wed, 09 Apr 2025 02:18:58 GMT  
		Size: 7.2 MB (7206501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c9b61f73d82f7415269b4c2637f0fc2b9abe111852a1cc8df3f69957b84be0`  
		Last Modified: Wed, 09 Apr 2025 02:18:57 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c450d5c7fde06ebc252fd939649c699d6e71d90e0b7f52d7f99a5b4d98f39578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265239748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0245dc89113709e05ad3e6b1d40e7b2c90029ce30478b57c3dbf6c32db4a9b19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c583047e73666cdc94eb0df609aa7d53eb0babfc52611f6c4d087a9ffda6db84`  
		Last Modified: Wed, 09 Apr 2025 17:31:24 GMT  
		Size: 143.5 MB (143454679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d347f80cf9922fdedef1c1222bd1840ef362512b93d3fbcd4423184c82461882`  
		Last Modified: Wed, 09 Apr 2025 17:35:58 GMT  
		Size: 69.5 MB (69529806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0205cf231e7a4f7cab7c34a34ba39802be7ef35ef04c17934bbfaff5948033cd`  
		Last Modified: Wed, 09 Apr 2025 17:35:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705d2bedfc4b1c2a86832fed040a7d2f86003b67bc5dfa2e3050441ce993eefc`  
		Last Modified: Wed, 09 Apr 2025 17:35:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b97d144a1fa04adaaaf4dc65fa229a5793d54267ba8027ad38fe0b80d70cef85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d3878eb118011c33db4366d856f18aca5ec9e6f22c211bed5c8afaa37c0782`

```dockerfile
```

-	Layers:
	-	`sha256:86cdfc4e8d988fffddb14b71af35f71d49139c113786117d27f51ea5c5c3f1a1`  
		Last Modified: Wed, 09 Apr 2025 17:35:56 GMT  
		Size: 7.2 MB (7211600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7017145f4fc71c7964be99dbf46ba94ee04d7d97948a2be51e7d71113e9fde`  
		Last Modified: Wed, 09 Apr 2025 17:35:55 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
