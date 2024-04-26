## `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:fcb999da24d4029457a371cd03c6880122e0826f1807be0d4552e26d702da4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8385e9eed5c852321b0c2b99e6e6873003404ee48a1501a6e043aa86a7780c9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235565180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd917557a585cb2143756facab0f776f366202c2e94d80de62fac4549a074be`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 04:44:37 GMT
COPY dir:e23ce7557a2e7bee9271385ae1512d655314258ebf585995b794db69e6e3d8aa in /opt/java/openjdk 
# Fri, 26 Apr 2024 04:44:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 04:47:06 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 04:47:06 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 04:47:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 04:47:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 04:47:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ca5178e945062d2877640df07eb097be0d14e566079a159d6bc27e6f4ead1e`  
		Last Modified: Fri, 26 Apr 2024 04:59:12 GMT  
		Size: 145.5 MB (145504625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2c2c1c83fc9c0eb8f0a71fb526567fad3875bbf191a057df1dfc43e8ff841a`  
		Last Modified: Fri, 26 Apr 2024 05:00:46 GMT  
		Size: 58.6 MB (58625674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb19ec20f6ca9aa8c071a4bb15b7cdd847f8474ae461ffd517ac4b08a5ba6bc3`  
		Last Modified: Fri, 26 Apr 2024 05:00:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:92e7fb0bcc1955a1af693779914e03e356e939921d954e056ba248331e8b2406
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231143273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c6655ca506b11e6d6045a8c8bf257c2a5f38390d3d6666ea76224611201df8`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 01:27:13 GMT
COPY dir:c78738cfcdd58dc875cb3f022a49b10c7fb9df08ee8a9995710ddf9cd16d96a3 in /opt/java/openjdk 
# Fri, 26 Apr 2024 01:27:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 01:29:18 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 01:29:18 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 01:29:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 01:29:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 01:29:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e94d451618b4dd0c08df5cf9a2e0c26b34468453511d78a90fbd5c442223d9`  
		Last Modified: Fri, 26 Apr 2024 01:39:24 GMT  
		Size: 142.3 MB (142306356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24eef060ecb7981b3453383bea3579063b61414ea88ff09ba6c0353cbe1db9e8`  
		Last Modified: Fri, 26 Apr 2024 01:40:56 GMT  
		Size: 58.7 MB (58748961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6414f274b28ffbcca8fb6ef7b664d771c916e1dbf6d18521eff1998c7a365a47`  
		Last Modified: Fri, 26 Apr 2024 01:40:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
