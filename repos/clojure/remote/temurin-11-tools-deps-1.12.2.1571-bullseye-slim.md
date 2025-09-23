## `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye-slim`

```console
$ docker pull clojure@sha256:5da34622e0649cdb067d9e3a7b586ae7e705ac5301c8ee1172acd705571eff7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eb20d80458d71746097640464376fec5b5a8f30f302359dcdc641a96ec895110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235068580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651490bd54ea2f03d12cecf223edcdb91275b54ee91708edb07d930d895fb803`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9eb11bd1fa9ee8648e080a7938c1975d61a3af5f2bbf0aaf9f26451aea501d`  
		Last Modified: Tue, 23 Sep 2025 01:41:14 GMT  
		Size: 145.7 MB (145658240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdce9b393eee2ecc2555856dcd1740f21cef88e940ab3181fa3ba9adf2fde388`  
		Last Modified: Mon, 22 Sep 2025 23:45:07 GMT  
		Size: 59.2 MB (59153626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c14ba0c3b6a466cf16c049a41f3bffa9e18b9bd10b8f9644b92eaa8d8410b`  
		Last Modified: Mon, 22 Sep 2025 23:45:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ac9acc8fec5c7d7e3eb8f14ac4999dfe0a96e2c2302b64ec610499c21d8da233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bdb046612b7b0e58e181e634b19f3619f4b6e6b935654b419ce8db29e38d95`

```dockerfile
```

-	Layers:
	-	`sha256:97f4b81f98ad8b9163921b720961b39552b4b5344c1a28f33b1d696126712ed1`  
		Last Modified: Tue, 23 Sep 2025 00:35:28 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5698d3d731cd98233d888bf2b0ba7af1989138caf8d31bd5cabf3553fc81b313`  
		Last Modified: Tue, 23 Sep 2025 00:35:29 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78651603dcb187226e440854a951976509fefac6ca44be25c4a74a1f85bc7422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230497090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b5b0a76fabbdf78063a90855e00ddbbbea8c6fcbd3168152c9970c83fc6ed7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b3bff4737e75bd7b6180f75e6d06de57969348f89a417a1816033ef79d952`  
		Last Modified: Mon, 22 Sep 2025 22:17:16 GMT  
		Size: 142.5 MB (142458743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732cecaa2b3368989cc5a2eb6dc7aaf59285e25131864e2f2444fc813eae6b77`  
		Last Modified: Mon, 22 Sep 2025 22:17:14 GMT  
		Size: 59.3 MB (59287244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becec1053c741f4b6d66837a09391d64c91cdf82c4c4e1cef1407f13704f3486`  
		Last Modified: Mon, 22 Sep 2025 23:46:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1571-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3cdf92237db41591c014d3cd77e364a385cdcfba66c65afff8feb7147148c163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59139cf3d224b7377768579f94307b7a319e3867feb43eb2735528398f631c3`

```dockerfile
```

-	Layers:
	-	`sha256:8411a5f006e3cd68da6acca6da32e8a64bbfcd42d20a5bda518b8f4c223ab703`  
		Last Modified: Tue, 23 Sep 2025 00:35:34 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbba71b911e7c192b6be79345c2308ba04ad4edc8842093cdf2a46ea084f37be`  
		Last Modified: Tue, 23 Sep 2025 00:35:35 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
