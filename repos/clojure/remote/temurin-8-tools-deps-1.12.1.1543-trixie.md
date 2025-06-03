## `clojure:temurin-8-tools-deps-1.12.1.1543-trixie`

```console
$ docker pull clojure@sha256:955b3dfe1a64826219e81d33432fa61bfa05075bd37dc73ee515e8c18308c956
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1543-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5dd74b1e61830f00788f833d626b65c88540d60368dc16c81d13796d14f0cdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191960907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28250d960b7fdf3de0cdac7c888c5428eeec256f8ddf58d563f303558d0b8c46`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62b438f9c0792eeeaa8637b24f8c401b4a12e19eef04c099112c78a727c9bf9`  
		Last Modified: Tue, 03 Jun 2025 10:32:24 GMT  
		Size: 53.8 MB (53830517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd29a9c6ba85f9dc89281e279caf294d3be11cab3af3ad1feef99d60a702d74d`  
		Last Modified: Tue, 03 Jun 2025 18:31:13 GMT  
		Size: 88.5 MB (88511451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27048e8415b4375d61f0053bca23c63e935f6c266b91dee754b6af70521d238`  
		Last Modified: Tue, 03 Jun 2025 18:31:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1543-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9119979c9d1843add81c1ac94e8be6865dbbb613a67d57f90b613ab28268c726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900c6094f372787b347ea55e26740c8ff38858e87c555ff5f96fa3dc839bc33f`

```dockerfile
```

-	Layers:
	-	`sha256:4390410a10b1e52533ef157a1964abde2f932e24761bac452d49e42b7389b39b`  
		Last Modified: Tue, 03 Jun 2025 18:38:00 GMT  
		Size: 7.4 MB (7447754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77555cb7b85132d353a828a6faadf968de57afb10094718dc375339889ac3d87`  
		Last Modified: Tue, 03 Jun 2025 18:38:01 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json
