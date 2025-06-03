## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f956d3799baaed4c320fa191d4434073711e7f69164383dd728a611f4a659cf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fb6a2e94b69db0a03c42fcf293e6763b92101de5fc9ece5f3f60575517ce733c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268785080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5591e6d452d1d73fdb4d93c5197173e6748d6edefd9c65f1fb31838080a794e1`
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da7cf9dd568b115f1f0074b658beb2d4b3b8a42ea1e180b8063d4c5367f6436`  
		Last Modified: Tue, 03 Jun 2025 05:15:55 GMT  
		Size: 145.6 MB (145635604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f2c82c4304198a36868cbcb3a6a16df39ae1be3a2521546518c8991d70ddb`  
		Last Modified: Tue, 03 Jun 2025 05:15:54 GMT  
		Size: 69.4 MB (69398636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068c7da7ec1077015582f5789e85c340c43222270eb74a9222f96a6d3f9460e`  
		Last Modified: Tue, 03 Jun 2025 05:15:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:79b1beb3df5159163a47f8c5faa430c0b278eed31940ad09c8298ae9140dd42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7290579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f18a895a4bd75f45362543b8598a892bda446723a1e8751e36b64303f4c3cd`

```dockerfile
```

-	Layers:
	-	`sha256:380ce661b045022429dfef4b942c644bd0ea4b1e5858542f8b7abdbcd616b358`  
		Last Modified: Tue, 03 Jun 2025 05:15:53 GMT  
		Size: 7.3 MB (7276327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b2d16b2cefedb9d20b4dc16cc9d07ee04e9b0aa37d9cf80e9001d0c29a98b7`  
		Last Modified: Tue, 03 Jun 2025 05:15:53 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f34a001d1710a40c2e7645937f4b399365267e8edcd2a0ab5ba322ad7e8f056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264199607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55af507b9dcb718aa3d4ba029c8f899ff585f584fa10da064f462ba7ed7f291`
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
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdd289c7253c53f059da906341840e1077ab6a119d05f64b8c6dff33cf8bed3`  
		Last Modified: Tue, 03 Jun 2025 10:41:56 GMT  
		Size: 142.4 MB (142420650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a268c244c2b982e5b30267c447a1703a5069a713289c2415a9f35adbb1dd5`  
		Last Modified: Tue, 03 Jun 2025 10:48:05 GMT  
		Size: 69.5 MB (69530557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a6cb7e8923bdc83a21792ea426e313eced16272213ab8e6d166a15cf54690b`  
		Last Modified: Tue, 03 Jun 2025 10:48:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c0838490f8e81d06c5fe353ab95c514a4f4713156e96443094f4a130847a588b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7296413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fa9ed80fa0dea4ef17c22f8b050229f06a3a790b9d4e110d6b1b40a9c3d944`

```dockerfile
```

-	Layers:
	-	`sha256:0615628c96fa6466e63aa4b7da3ed0fa8a7b052d737124f45dff6f92822046fb`  
		Last Modified: Tue, 03 Jun 2025 10:48:03 GMT  
		Size: 7.3 MB (7282044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485475720e057443a4f1e0f00156b812cfeaaf4757b780f0db55910a073efdb0`  
		Last Modified: Tue, 03 Jun 2025 10:48:02 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json
