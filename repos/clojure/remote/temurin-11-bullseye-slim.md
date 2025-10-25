## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:6e9ace49cb0debf585250812092b6694267aa1213ff70330316e98649998b9b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8d3f1c60c508a2a6f9dc663d6ea57520a0a2e365f11a8a806ecbea019874ae62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235068055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bd902f3d21a9e6e996ca32565aa98779da1003a32b3be3af577046f3ca0ccd`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404ae972abc126351c341f5572f024cd50fe913ae6c58430c4ffda7211e31f38`  
		Last Modified: Tue, 21 Oct 2025 13:01:01 GMT  
		Size: 145.7 MB (145658349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76be554fb63a05b60ab200a16ba0c0eb7f596c335094fc11715a838a28997a5`  
		Last Modified: Tue, 21 Oct 2025 02:21:35 GMT  
		Size: 59.2 MB (59150696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bef69cd292eb7c1f686b542490342163a3f0034e30cb3eb90c4ff860fdb2ec`  
		Last Modified: Tue, 21 Oct 2025 02:21:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4f6d36f7a3e73758bd2677092ae6e05d711abe804c8d91c82576f7fa1b6f7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235839c0bb625805011f7ca347802a6cd85d681895844b4da0a2a6828088c880`

```dockerfile
```

-	Layers:
	-	`sha256:df7b1c64195cd1f261e21ff120506064599c9ec7731380123ad1df3e154e44a7`  
		Last Modified: Tue, 21 Oct 2025 09:36:08 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1ffba70db2580b620ae20faa771fb611ec771969ac337a3b92a41f70b26eed`  
		Last Modified: Tue, 21 Oct 2025 09:36:09 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e380198777c93f4afd4faf14df2768d42e333d2e6904215f350c97519f8344f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230497179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22b70cef7a706973574ab974b8580fd04140cbc189be50709daa117596b796c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc52b84a12fe7ce1498e3b4d11c0dadaf3b2ccbed26838e186c619e63e31b71b`  
		Last Modified: Sat, 25 Oct 2025 07:23:18 GMT  
		Size: 142.5 MB (142460578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b2132919b75b14468868ea37958935b130e950ecac5069ca201b78abd58ff`  
		Last Modified: Tue, 21 Oct 2025 02:26:59 GMT  
		Size: 59.3 MB (59287557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51033a75cc3916731c83069ec51a02c162ef1232598a6408736c3791d8147248`  
		Last Modified: Tue, 21 Oct 2025 02:26:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a565c8cc673cd1372264107bdf379bdc8a07ae6fa9fa63f9ef84331505060ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc488c6ce9491f26b27b383420b9cd5ba1e80b069ef46d4cd103658434dc00c`

```dockerfile
```

-	Layers:
	-	`sha256:97356067d4006280a4d04abdb7925561fb87d6555d3d2b9cd8b8fa4b2251529c`  
		Last Modified: Tue, 21 Oct 2025 09:36:14 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae4fb007b44b5979735f82acbaf71fc55e1e856681fa32ff5b05dd315bbf4ae5`  
		Last Modified: Tue, 21 Oct 2025 09:36:15 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
