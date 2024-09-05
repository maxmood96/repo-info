## `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm`

```console
$ docker pull clojure@sha256:e7ea331ad0eff6836b3bbf6f585e27284f0e7e17e7f47b9188b9e412a02cb380
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:179054d1e54496d55f89b3ab2001437380a1a0323639f27e9468e00146c5b5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233635352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21352f4234af77a57727386a8400986ad2b5bca93623ae21e8572291018dd4be`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee80b11682ec0aac86c8b4814e12b5bc519207f79c40360f234ede7732ce3b6d`  
		Last Modified: Wed, 04 Sep 2024 23:07:41 GMT  
		Size: 103.6 MB (103611881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4586af28ed4f657a16c307a41d8e6f328efac5d1434f969e8fe968fdf246894`  
		Last Modified: Wed, 04 Sep 2024 23:07:44 GMT  
		Size: 80.5 MB (80466123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8c72d376bb2b9af81ff079d647cbf35aba92cd2af686d49cc9faa7f9ce9b1d`  
		Last Modified: Wed, 04 Sep 2024 23:07:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8c0a2e9819b425ba593b6e886ae216f79562664c30bdf39be97c2f1d34db0c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7038813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a0f3320aeb162aa9df2c2995e2125a36488e8320ed26ea8b2912c3d658514c`

```dockerfile
```

-	Layers:
	-	`sha256:eb9417aeb5001d883b5702237cd1f15bcbea6211bc354dcdcc3aa7c0535a2f80`  
		Last Modified: Wed, 04 Sep 2024 23:07:43 GMT  
		Size: 7.0 MB (7024962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5d31bccaad0dc0837909675b40fba5b033ed3342b8d80852a8e9f18d98e1591`  
		Last Modified: Wed, 04 Sep 2024 23:07:42 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e8d69dae76343f33da7b072e4a033c756f4b407c4168cd44617c808833456a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232516912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056906c0df352d6963f6aa3bd4f3383fcd25efe0309f9ccc248203a73834b9f1`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df82fcaf825bfd95bf3f6a60bf33b338e56c6f56d64178e49f0cba774c6851aa`  
		Last Modified: Sat, 17 Aug 2024 05:50:41 GMT  
		Size: 102.7 MB (102729249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f746f1a501618a4a44c5b26b39e9abbdba8041db75216d0611702cacac1e7608`  
		Last Modified: Sat, 17 Aug 2024 05:56:15 GMT  
		Size: 80.2 MB (80198427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22810dc900a5792ba8b6288c5805112f448f03e6edf91c827e68f28b0430292b`  
		Last Modified: Sat, 17 Aug 2024 05:56:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1c9775c2401681b28c72bd3f3ccbf25df7bc11952deaebf0e40dd22f7fd5be52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7046350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d32b38cf1d6086503ea32d34872ec7292142c10aed83fe3a4832f01877dbe0`

```dockerfile
```

-	Layers:
	-	`sha256:30558b1e44a64d5a4ea68e90396e92f488ed3acbc4f46e0ad8b7606c69cbc042`  
		Last Modified: Fri, 23 Aug 2024 20:46:55 GMT  
		Size: 7.0 MB (7031964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62ff756d2945c891c2e320b622c8637c7e80b0842accf9effe2abffc587d0a58`  
		Last Modified: Fri, 23 Aug 2024 20:46:55 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json
