## `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:33a5c60fc0c67cf54d3536b5ab28da37ef6a8a3217758289f3fb5a46bc6ef32f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:64d7399564a18e6eee2eb6502704c09b0f5e517b1b9bdb2d7e213ad19ad83241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143972131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e85ba74d204b865785aaac2c1d0344a1b989ed3ff70c7c5a81673ac645af03`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db53c705a9d628ac6757c867a624798248461802b072781bb9075866143d24f3`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5c554043bfcf1ce6fcd18e1064961e3489afad622401467da3f880cba26bf8`  
		Last Modified: Tue, 08 Apr 2025 01:35:19 GMT  
		Size: 59.0 MB (58992834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659be8ba725808debe79521bdfdef6cdafe241c30c49872db333218f12d4a182`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:060569fe1313c48c2605a6a616919c8c8a32eef2ce1d605df2374d80a185212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8118f552fac3a95072f7932bf7a57d21a95c7129b08dc5063f8303dbcdf0e9`

```dockerfile
```

-	Layers:
	-	`sha256:99985a344c510d9d78666b15f4416754b319d8b0c776283222d0ebbc1a3f7b52`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 5.2 MB (5240623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ae5f90288dfc190092c4f8f737358ffca99bdd1e0d7bce160842e31c68f565`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eb3150c98ffaa59812af358be3678cdd1c2d3dd0ce2793a2ce67ad05eacbf8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141700375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbeff03bf4f7f4403142f082dfebddaac0d2fa6a13849bec8379f870ae97ee7`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b740635662800cf45542e003160b097654017b23adcb55673545e559db86e4ea`  
		Last Modified: Tue, 08 Apr 2025 11:14:43 GMT  
		Size: 53.8 MB (53822750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf65d3cc751b1075968eb0f5fd3d5a8852c26f2eece2a83a8b65b64404b23aa`  
		Last Modified: Tue, 08 Apr 2025 11:18:19 GMT  
		Size: 59.1 MB (59127482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c37213c71d6e3850152d545bac65bf19586edee8e1f9d402e309661577f6053`  
		Last Modified: Tue, 08 Apr 2025 11:18:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e198f55e47013353e3603acb76cbe549399ca0fad32a3b2ec376765af4744f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852aadfc7b0a18bd74981ec14618ab5fc1acc10f543598c8e257b6c18d20ee3a`

```dockerfile
```

-	Layers:
	-	`sha256:d6bb57ebf907b38ac8599c526598e3d65b11693b77e59bb0d7c48ac76eac25a2`  
		Last Modified: Tue, 08 Apr 2025 11:18:18 GMT  
		Size: 5.2 MB (5247053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81eb1872900cdb9842fb8007738de039ed9fafe545b7f270ea79441e7f7a066`  
		Last Modified: Tue, 08 Apr 2025 11:18:17 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
