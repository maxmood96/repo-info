## `clojure:temurin-11-tools-deps-1.12.0.1495-bullseye-slim`

```console
$ docker pull clojure@sha256:705b898b03e7f6e1878c9f54f82fcfd410479fc00098a73d1b640432d85ce49b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1495-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6d21142838eee00ed3c8d9e15a4934f4a5ede09358d5fa84098a1b73b79cbe17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234635869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b886358b8a1ccebb42dcbf029cada352a8738186ab6dd95a46f30ee8369381`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8912702c90376ca69d3763303cf5180f77a09771a3d53e1b984e988213522b68`  
		Size: 145.6 MB (145601466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b7ce076b8ff5502afba19d250f2f1a7adcd40c21571311abe25187804ee481`  
		Last Modified: Tue, 07 Jan 2025 02:29:19 GMT  
		Size: 58.8 MB (58781117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9851c0c62c08a10b1527e33b5cc67ee70994ec23c2ff9813abaf2da20c9b77b2`  
		Last Modified: Tue, 07 Jan 2025 02:29:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2bb9b02e274d5b322d30687d5591875604581ad8a2bd74e453c8b1eb5dbe451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9ec0ac311c09db58dfa36b792fb2f140e61c8b8de8c505d72d4121442d00ed`

```dockerfile
```

-	Layers:
	-	`sha256:2d3b81e86eed9ce707a39c347f4c2079f79d0562236f8c282291ca16d49658bb`  
		Last Modified: Tue, 07 Jan 2025 02:29:18 GMT  
		Size: 5.1 MB (5137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1549612c7f9f57c2325af97c00eee219ad14c23c0378a568717fbae487137dfb`  
		Last Modified: Tue, 07 Jan 2025 02:29:18 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json
