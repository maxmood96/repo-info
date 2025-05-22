## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:9b8b5187a7c0847cbdbc5c390b1aed43a0c01d6bda835326e9d7b96dacf93f07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0dd6f1c1c642cf6a4d144bca13e28fc46500b0b2591b36b842a3a43107a94dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156195349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a6aa9463ec46b0c1a209952adb72e1f13a90be598d306831e2e6104b633fd2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33ec3b2cf56ad31185f65db380fc5018ff1fee91bd1a06a168aa95e9bb13dbf`  
		Last Modified: Wed, 21 May 2025 23:31:59 GMT  
		Size: 54.7 MB (54716171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a287b7206ad22f3ae97f4d8b3a03975bd9edb493fe219ccab1f9c0e8466a59e`  
		Last Modified: Wed, 21 May 2025 23:31:59 GMT  
		Size: 71.7 MB (71723151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980e96392f57937d0bee8219107e83149b053349c5a740354dc78815dad86cc`  
		Last Modified: Wed, 21 May 2025 23:31:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7722f038771709dbe80b5943c63cb9237b7da9d796dac9d92f557e7f40816f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b6a627ff0dfd3d51b608b8dfe613ccd0ac345722abb6bcdf030f41c25cd4dd`

```dockerfile
```

-	Layers:
	-	`sha256:32f168bb7e45b74b6b359e0bda4cb3bb4fba8a7715bde9687353e8e6c84855a7`  
		Last Modified: Wed, 21 May 2025 23:31:58 GMT  
		Size: 5.2 MB (5233675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f3e621bde092cded2b45361951abed5881d3fa53508837dc47d0643579234dd`  
		Last Modified: Wed, 21 May 2025 23:31:58 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66537f8d28917f8697ff6922f700aa1147dd755bd4dfe37d59fbfa85dd755713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155597474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357aeef673958af23148ae69d576ab602653647a91c39f5f3821b51b93560b72`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Wed, 21 May 2025 22:31:23 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1510a979eec55c1e74fba48e30c2b829ae1501a30aad31695a963a03b2325099`  
		Last Modified: Thu, 22 May 2025 08:04:19 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b108efd64759945348dde0a61d29aa58a8f285a75be707939c80cd30dc9cdb41`  
		Last Modified: Thu, 22 May 2025 08:08:39 GMT  
		Size: 71.6 MB (71646858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddd86793f441a5c77e3d6b64b28025c94c03e15f429622c856e8955a64a0137`  
		Last Modified: Thu, 22 May 2025 08:08:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9520a46cf63cbc80d5ca207dc477d619af7d103c9b7dd8c7d786c4f7820e1d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da5297617056bdb884a4510d0ae034a39b8d9e19b596d699243ea8aef5e7bc4`

```dockerfile
```

-	Layers:
	-	`sha256:731fbe8ec0ae5acb3fc9b4c30de28cc4103546d508acf02a66dd06b7145fde0b`  
		Last Modified: Thu, 22 May 2025 08:08:37 GMT  
		Size: 5.2 MB (5240142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a585b5e769a46913197ae41591bb38da742fcf99cc4be28c931b78e3525271`  
		Last Modified: Thu, 22 May 2025 08:08:36 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e60429e6b1cb3c21cf84d316d813f9e590327bd56bddf7b881842494bbaf5afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162961625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bdbb9a5d132e6cbfc6664b0aa2d841542e6f166bf2db1c5ce06be2ee381fd0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Mon, 28 Apr 2025 21:25:59 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ff01908b868a75c17f94ffc5626215722b986fb8c1aeb2606b9cecf365a22f`  
		Last Modified: Tue, 13 May 2025 18:05:52 GMT  
		Size: 52.2 MB (52167960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018011cfcd35b42fdb01b9646dfdc8ecb23442e15d2995a8f8fb9d74469db0f`  
		Last Modified: Tue, 13 May 2025 18:20:25 GMT  
		Size: 77.2 MB (77215326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e3f0ddce12cdc2805b643c486750bfc5e42e84d439105387608faa95621f7a`  
		Last Modified: Tue, 13 May 2025 18:20:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d55a97bdb7f9740d7483eb3e9aa6cfe0c56ffe0a30fad92a328b544d733a5ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff2fcc0864d8658074e1f0e97e2fd32942aa354be90e2eb49387896d8707206`

```dockerfile
```

-	Layers:
	-	`sha256:45d2d752a8a9f98f563b70e1d88250b95b67d8c9a29acc167f6a29075c7e584e`  
		Last Modified: Tue, 13 May 2025 18:20:22 GMT  
		Size: 5.2 MB (5193099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f8ee2b63c18e3c61e22e678fbb056c3a8f0bccc3bc8924b1584f7471cb41f3`  
		Last Modified: Tue, 13 May 2025 18:20:22 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
