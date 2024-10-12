## `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:af06179b1aa0f9210ed65984331d4a665090a308b36544f913e88164ee61e0c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8dc5a75aee5bdc023b070b79d79f019d45763916e150c322568de7b4675b02df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275650883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6475bea95ec21b8374a3a6cbf2c4952d962c9ef1f6a9576b47bac601d20e3d27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f615bca7cc6234a7f39529384835207d70afb35e538db31626f51ca548e3beaa`  
		Last Modified: Sat, 12 Oct 2024 00:53:51 GMT  
		Size: 145.2 MB (145166553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8e53a04959771ccad153566ad34fb55bbc5e0d1c2f8d5a5c010a2a69bc1a64`  
		Last Modified: Sat, 12 Oct 2024 00:53:50 GMT  
		Size: 80.9 MB (80928237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba149290019fc854f118e4ae42a26c1f0b1d9bf9ad7edd1325f0bd9ac0f8793f`  
		Last Modified: Sat, 12 Oct 2024 00:53:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5909498978bea93701fd51b68935a54f4377e2de9a6da328b72bee6762c0c86`  
		Last Modified: Sat, 12 Oct 2024 00:53:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:370f9463a5ffa91c4b6b17376ac4b4b1219187528d2e3254de99f34e0ac13261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7171482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e99ed69dd7eca612ab5d4fbdaaf25b57d885be8ff8a3145b10b36a730a1d61f`

```dockerfile
```

-	Layers:
	-	`sha256:be6100ee24b490c0c3f37f99a7b8f33d9cb1f4b3d597ed33554b08a5a76293de`  
		Last Modified: Sat, 12 Oct 2024 00:53:49 GMT  
		Size: 7.2 MB (7156006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18816a08bf50cd2012fcc20f9cba0e899ed6be29bb5e2bd1125eccf13c19bd7`  
		Last Modified: Sat, 12 Oct 2024 00:53:49 GMT  
		Size: 15.5 KB (15476 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:218f8fe6238c31ae05997cdeed628128851f72924426aadcf77d66d6dd6948ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274335718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296d953275b5f1622e98cef26f8f2ea18a0d77b7e18e511e0053d22090d9906a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4efff08b7942d97fa8379eaa17c2bf6fb8ca57486eed169075310e192b94259`  
		Last Modified: Sat, 12 Oct 2024 01:13:37 GMT  
		Size: 144.0 MB (143959514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0036cdc2edd1c250a6bb1d35982c60be6d1dc29ac9f288a00be4b383518e566d`  
		Last Modified: Sat, 12 Oct 2024 01:18:20 GMT  
		Size: 80.8 MB (80790273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c78567b0b8ab33dc6eef243e06012a475152fe6f9eaf2fa90506159adff4ff`  
		Last Modified: Sat, 12 Oct 2024 01:18:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc3ffa1d7eb7708d8adf310de9146f6619825224f7ed0bf2503a17cefe57cc7`  
		Last Modified: Sat, 12 Oct 2024 01:18:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:441e640a3ee6806692357de1745b18ed5b049ad45312615eb0e5f65265b2920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7177358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eee795c18d4df4fc7059a8b9a7a21dd1430895d12e7175e48f61f68c40be92e`

```dockerfile
```

-	Layers:
	-	`sha256:1959acbcadac2fcdeb4e82396e192e793479d10afc1876d38cdc266d9ed9f350`  
		Last Modified: Sat, 12 Oct 2024 01:18:18 GMT  
		Size: 7.2 MB (7161774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1a43d42b1f57c6c2df109f0521198e8dc665704a0ea9b8f81dcbe816621bf6d`  
		Last Modified: Sat, 12 Oct 2024 01:18:17 GMT  
		Size: 15.6 KB (15584 bytes)  
		MIME: application/vnd.in-toto+json
