## `clojure:temurin-22-tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:5029fb0042efa36a0df3ea7456bfb051e880b9b90f93f1364419c00d2b6c18a5
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
$ docker pull clojure@sha256:f4195fbdaba04034d399701c661a9aa9d68070c55976e5b1a5950f211b525570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284880408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e50569b40628e0150088772cf9faee7a96d203a9418f664ddc42fa5a17ec11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c8c9eda89bce9a9dac276486d731e8a2490a3a7a645e69f0a76a24296e771`  
		Last Modified: Tue, 17 Sep 2024 04:51:55 GMT  
		Size: 154.5 MB (154503778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00c31d2ed78a7b0a26ea25a6a057830ee6f99022f3cdf7686e3f34311d546ce`  
		Last Modified: Tue, 17 Sep 2024 04:57:47 GMT  
		Size: 80.8 MB (80789962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debd864c65e32cc45a0fa5399e0f4668376eca0c8032dd9166719b614a458021`  
		Last Modified: Tue, 17 Sep 2024 04:57:44 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ea758fc4f62a22e3ab1fed039f603073e8357d1ecda19fb2b51cd189a26d4a`  
		Last Modified: Tue, 17 Sep 2024 04:57:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:7a34423c1368408d4360585e9a18ac7d438e3da6dc02c749f88f2a4d49b77a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7030760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06010630939a30854ec6f26014547d9db375c858d9e4899fed2cd828d23e92f`

```dockerfile
```

-	Layers:
	-	`sha256:4cb5574d07b4b17f1df221ccf7f7bbc873e9671f5749e16597d99ea4bec66ade`  
		Last Modified: Tue, 17 Sep 2024 04:57:45 GMT  
		Size: 7.0 MB (7014076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b36faebce44745ffe7103e63cf6e5068b397b716e3bfbec0587611417a2e9a9`  
		Last Modified: Tue, 17 Sep 2024 04:57:44 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
