## `clojure:temurin-24-bullseye-slim`

```console
$ docker pull clojure@sha256:c865b80f85f8cdc7f6f42448c3e46caf37ae942730800f03f68f0c4182c2801c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a948fdda1e444882cf7163b9f76d87e1fd346408586981afb41864f46d384709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178991756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee92eabaf667f2de1fb1fa1d9f20b8a36b3ce4aaf32f12d8039b989b10ff57c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9826c65fc900402d45588b52938269dd18e0678de9ee70c16bffaff90e12f7ce`  
		Last Modified: Thu, 27 Mar 2025 17:53:36 GMT  
		Size: 89.9 MB (89949033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dbd1273f4fb18b4ebc72aa2466dd5fd955e2b87736e98154b344c3567c83b5`  
		Last Modified: Thu, 27 Mar 2025 17:53:36 GMT  
		Size: 58.8 MB (58787844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d326f55d0018b994c52aef1c5975d022239a68c93047d2b62d9d16633a4bc38`  
		Last Modified: Thu, 27 Mar 2025 17:53:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d45375fe8c4f5db6f4034a77d4ea82cc7abd2071ca104f98cd0e8115d1501e`  
		Last Modified: Thu, 27 Mar 2025 17:53:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44a0097eed583fcf12ed1c9e80f86d9d03a475b4797f96592ff5f399587dbba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c879d2bd18b6e935c4482cdfd96c6710727967ec350f862fa221625ca9844734`

```dockerfile
```

-	Layers:
	-	`sha256:00f815b0acedfdc59abe025c3922997efe9cf0a73c11953465022b0df30ee816`  
		Last Modified: Thu, 27 Mar 2025 17:53:35 GMT  
		Size: 5.1 MB (5067699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c99ee402915ecec40c10e58cc92cfd9425cf3c7620ed7a986c920570df63a40`  
		Last Modified: Thu, 27 Mar 2025 17:53:35 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ec648f5963d164ab9d3f2385c23957a4639d452c88866d990fcf507553c0d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176761150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522f1a24235de67e49a60fe0a4d35d16be852934de9a21ea5f51fb0c911f5ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810ff949c882dc88620936ab3b019fbb2b39d872539a484496b86f21d29abbdc`  
		Last Modified: Thu, 27 Mar 2025 17:56:15 GMT  
		Size: 89.1 MB (89092702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f63dc4f9f6ea1b454e32d67dc99c67da24568c23189ba5d91d462a8f421b1`  
		Last Modified: Thu, 27 Mar 2025 18:01:08 GMT  
		Size: 58.9 MB (58921484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5913ea595c019b2d096851a0ccd9096767d90dc90332dd5d2c3586edd45fdf51`  
		Last Modified: Thu, 27 Mar 2025 18:01:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f2dc6cfd6ab32b087d4b35dc9921e3bdbcc4f3a03f2b1e1b96a4a8cafbafa1`  
		Last Modified: Thu, 27 Mar 2025 18:01:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ffdb5b2cace1fb5d505fd265d3b43ea49d909809c05170bb4493d011ab8912b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabe41a4ec7494357483dc668279c7b989dbd870e5cd768ea360a18e2bfb3e56`

```dockerfile
```

-	Layers:
	-	`sha256:1cba9086828c3d57f5104ffe266380b8b822d3060da232dd47a0f670ad587509`  
		Last Modified: Thu, 27 Mar 2025 18:01:06 GMT  
		Size: 5.1 MB (5073428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf3fb1cfaca38fe9661ba04000dbfdc3dd191626136e9ccfbe13a4809a306649`  
		Last Modified: Thu, 27 Mar 2025 18:01:06 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
