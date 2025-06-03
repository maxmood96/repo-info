## `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:6f2add11ada1d5956c18cb6e20ddcc49dcf2be60d26ab62aa30090ca90253bb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5feee77ec8ce104f5b1b1bf486d86a07491a6ca1de6499fcc89c369ddb0e0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177865570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c9fb4d3f78bd665394710ec82acfdae1447b97987416bed5c4e25d8be1ddd0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1774e4582875ba2932dbcccaa5df9198f7fe57563244475e76804db5509d67`  
		Last Modified: Tue, 03 Jun 2025 05:15:36 GMT  
		Size: 54.7 MB (54716189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a3116a21ebfeae7ed632e765e1ef8d58e9d9c4450b6727047fc746e5d23987`  
		Last Modified: Tue, 03 Jun 2025 05:15:38 GMT  
		Size: 69.4 MB (69398544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5778f503e1fa1747bff5265e9fc4291be8853eec89adeb4be0e2604ee6c019e9`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1a3abc7fbae798904637fd068e428234b1c94d42b65516d254f67ac073c9338e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ac7ae4b001e0d0b9fcbe6dc5f35bc0d7ea9247c8a4917397bac9e258699e78`

```dockerfile
```

-	Layers:
	-	`sha256:2d19aac52a15dd3d0704bce511e7d7aefea5d6d6c2c23492d8c9854b6cd57a1c`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 7.4 MB (7377796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b5b515d0dc0e4beac3f4a49cc5985598be512fab429c209e017a2b15fbc365`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5bafd488aa88f0e06ae29034244f0a5a689d49c2e9041d8147b5a9ab8903f3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175609684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f62f25c22ecf31651024e66689ae5f5169a006034a5fc9b88bdc7bfa308689`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ffe9e57bea5c2829c0e806cd1cc2d099c39a0f58f107bed7af9204a03c40b2`  
		Last Modified: Thu, 22 May 2025 08:01:53 GMT  
		Size: 53.8 MB (53830517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab37e00c228064a5242f43e30e99a3c392b29f9a08e64a546497805bca515f0`  
		Last Modified: Thu, 22 May 2025 08:06:24 GMT  
		Size: 69.5 MB (69530767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24be7ad7807535a9047d9a93fce3a68a9ca91d23b5ff310b4c7868ff0a53ba1`  
		Last Modified: Thu, 22 May 2025 08:06:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1b96f217d1c2d7c1010e24849905ab0e5c895ddfa791471198443579992395e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164ba1cf8536792c1f84e39f77ee4a1397212c8e2aa06d29515fa76b756cdda1`

```dockerfile
```

-	Layers:
	-	`sha256:cdc773342d3917273caa4fbcab4ae2112b46443e6135a8ac9bf0c7bec127cae6`  
		Last Modified: Thu, 22 May 2025 08:06:23 GMT  
		Size: 7.4 MB (7381997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45aaea10e1efa3178b8830fe374e8ff70dafc404c31e3fd5c4e29f09576abb41`  
		Last Modified: Thu, 22 May 2025 08:06:22 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
