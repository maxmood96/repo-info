## `clojure:temurin-22-tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:1c2225dd986431f90dbe6217338148c14b8b889574ce77bc8457d3b5b8ea4d32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.12.0.1479` - linux; amd64

```console
$ docker pull clojure@sha256:8d13e07d02c74539efee611cfb8dc1dac41a485f69f0c94270aaf1d48e5f5194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286965886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d6abb18b5c7f49f27d2d4e1684bdadfc5b40bb4de4ea0e15d20f2554b4d7c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8aa7cf3a9439146a2b01f437e9c076be2646a04e9b60b07f623b05bf04517f`  
		Last Modified: Fri, 27 Sep 2024 06:01:26 GMT  
		Size: 156.5 MB (156481659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54328026d179015f74f298f7ba4dd37a003d72f2487ce341d88d4a039f1b627`  
		Last Modified: Fri, 27 Sep 2024 06:01:26 GMT  
		Size: 80.9 MB (80928138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec9b086fad9f7b5038ee3f056b3ab4b0c6edd993c95bd24ca442d74382f5a62`  
		Last Modified: Fri, 27 Sep 2024 06:01:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece38875fbf5f9e613381866f79ea434f2883b0d621450d9919fa4fb9a46da85`  
		Last Modified: Fri, 27 Sep 2024 06:01:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:1173361053be4544f2823b5e9ae4cf997eba6f1b9220c3bf88dbd1dd751e9038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7177157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b7a0a51229ebe0e2215bff81b77183de061e398a3a3987731fc713bbf56a4d`

```dockerfile
```

-	Layers:
	-	`sha256:c85d8670aeadeaa6b992dac182e8ae1226074a3e0c29fc71e94819a91418cf42`  
		Last Modified: Fri, 27 Sep 2024 06:01:26 GMT  
		Size: 7.2 MB (7161033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a7e89868033f2a28dcfad93a461f7dc83ad486204d4e8b7148ee63269feab4`  
		Last Modified: Fri, 27 Sep 2024 06:01:25 GMT  
		Size: 16.1 KB (16124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.12.0.1479` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a3330995573b961ecd1e4068a0d8de97ee84c28ce784a31f2b5a6a56db9c55e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284880012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f94027674edd8db2aa30da185dc42bd8877d401345d4be5c8e1bbe82db2f3e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecae5d232710afddc5ee0c06fdb21e26e265b84f1aa73e39ee2824c5fc231de`  
		Last Modified: Fri, 27 Sep 2024 10:46:33 GMT  
		Size: 154.5 MB (154503777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e87af69bbe04fa9bd2418101612ed95f4bbc45982e9ff7b761b81ab2291e08a`  
		Last Modified: Fri, 27 Sep 2024 10:50:30 GMT  
		Size: 80.8 MB (80790312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28494a60dd64aec5dd5a6df12bd439e7500425a1efe550df6d515405d9f66136`  
		Last Modified: Fri, 27 Sep 2024 10:50:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ac031bd2a24c5bb414c572fb3ae7d7de334d2db3d672484b5bb6084a1c044b`  
		Last Modified: Fri, 27 Sep 2024 10:50:28 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:511dc7ff745418c9da135ba35e0a5fd77de3a69d494a1cc5ceb100fedba4aa9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7182887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d61460e593e696227d424dc0be8ec283018c56a0c66e29116708dc35950cdf`

```dockerfile
```

-	Layers:
	-	`sha256:fffe71c8703ac8f1cb920a5b81a58f21e770fff3e84e00e8b41750ba34775fcc`  
		Last Modified: Fri, 27 Sep 2024 10:50:28 GMT  
		Size: 7.2 MB (7166203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bc7d44d80a3cd1f26f48a6fe861adf25aa6967a049435ee94ebc404dac7f87`  
		Last Modified: Fri, 27 Sep 2024 10:50:28 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
