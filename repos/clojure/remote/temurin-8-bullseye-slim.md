## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:b4b9f781b415a2462ad5253af8e92b4ce33966dd304d759f16c6a243848ef21f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:54403e2d541bf111e38005488821e8937504270d333d74768202cf1cc770fc5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143760713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058d76408a627a6165b1f6daae0e87195898ae922d715f9482a61c7e34bace61`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a90f7e1a94a389a7cbeb5a03a0e35a4c597983adb6315bd3c8719c738d9e2`  
		Last Modified: Mon, 10 Mar 2025 17:39:59 GMT  
		Size: 54.7 MB (54721226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75592af410595777eecc8fa17375e667be2cfd625e74ab88043046187f2865ee`  
		Last Modified: Mon, 10 Mar 2025 17:39:59 GMT  
		Size: 58.8 MB (58784908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28eea80aa0e4fd451b02f9d2234d3920ffc2fdaca87bfde885d58be999518d91`  
		Last Modified: Mon, 10 Mar 2025 17:39:58 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8f1b3f0c2be6f751c813074c40b8b15cff25de2090fc09dd93fe1ba8118fe748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361c27c9f5a3a2f240448f3262cbdf3c0f9d845d352da5025aafbf73322e5b30`

```dockerfile
```

-	Layers:
	-	`sha256:db3cc9a9661b376714c779751029cc3b7e71c8a8470fa10da6847fdfa0c44be3`  
		Last Modified: Mon, 10 Mar 2025 17:39:58 GMT  
		Size: 5.2 MB (5238677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb29d0c2652429d92fe2709581dbc2214ed49c768d5d0c3ec59a58a3402cf050`  
		Last Modified: Mon, 10 Mar 2025 17:39:58 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9ee23d42937492ad67809aa1b1006418e3dd5beb7e8235f4ad9b97b13a50f391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141477796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3d4d61c3314ad5dc10517b3ecda7103c6a2d2cedc2c8beb41fdbf44f494950`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10ad0ab2a522cca86eb22d65591c0e263caf1a0c4a60c014a3f8a6e470171c0`  
		Last Modified: Mon, 10 Mar 2025 17:45:55 GMT  
		Size: 53.8 MB (53822750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5a04115e9b1fcf8f1400a34318caf6237dfd9243ce55f92de9ccedcd7f2749`  
		Last Modified: Mon, 10 Mar 2025 17:45:55 GMT  
		Size: 58.9 MB (58908412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90e4c8b4a60dba3d8a62d9d935ca0493980d53b0c3420210e718af730f0a335`  
		Last Modified: Mon, 10 Mar 2025 17:45:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d53cf37c948e97e54d69035f2051ebdb2e7177e53dab71adbdbbb45366688a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc10757baeb8297bdc632130d297ac6124b8e09b7fe70a3c25ecd9b052e8a0c`

```dockerfile
```

-	Layers:
	-	`sha256:80e6192b7efb33e5d67773048e7878b6e442b432d6d8acad35804a3d3a5d5be1`  
		Last Modified: Mon, 10 Mar 2025 17:45:54 GMT  
		Size: 5.2 MB (5245107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97df79b90c2c364ea81935c8d59395b949507d80eeeb4f673caec6fb3ce0378`  
		Last Modified: Mon, 10 Mar 2025 17:45:53 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
