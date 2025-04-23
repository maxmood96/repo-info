## `clojure:tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:1deab177966e0c0706a22f8cd3592045b421235fb7f9fcaa1fcf8d7230c3a670
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b83ee9af56629459fac64a98d7140585891d4e1c1e267818305f96dc69de4828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280778951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ff3b4a500b38c583b634cbdb5cd864c7e42216c800da06d5c1ef6527f97719`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bfb0ba483951dc2025872e297a40f6ee8465b6c65f5b3f7e27be7ae4e49a74`  
		Last Modified: Wed, 23 Apr 2025 17:16:46 GMT  
		Size: 157.6 MB (157634442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8323f1833382cfebb922c23122fcb1947630e054be3692b3ddab15fcb8c3d779`  
		Last Modified: Wed, 23 Apr 2025 17:16:45 GMT  
		Size: 69.4 MB (69394936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2c5ce9cf9ab1ffbe36964dafc0ac5a32cc333b11c188da842da32067371f5b`  
		Last Modified: Wed, 23 Apr 2025 17:16:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c634bc5663a7cef77c670fe7fe4a22fc22e0f7aa303b8bdc1180e3e229e3e76e`  
		Last Modified: Wed, 23 Apr 2025 17:16:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:61bd0be4f3b6dd40c59459a7d535f017d7f0aa608ab3c1234fb278535ebde2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7226776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30f7b7bd081cba46df0bcd33eca247a9c0f5f7316624252176f4c4bd4b39827`

```dockerfile
```

-	Layers:
	-	`sha256:5ff61725737457849faaf688e49e9fcc85a1e2fd40e481b9746bd5797f1bd570`  
		Last Modified: Wed, 23 Apr 2025 17:16:43 GMT  
		Size: 7.2 MB (7210279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f6893b03b6bdbc575fd97f378052a82e4c131bad6ca37ad9255253d5663bb95`  
		Last Modified: Wed, 23 Apr 2025 17:16:42 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45e10902ad26bc784fd8b1e3dcafcf8a5a2748bf3f9d1e3e41ffec8a4c7a8ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277713256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48245567f4f977dfa488469fb7e59cc1a781d4b87507fcfa41b6156740792a02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2361802ed8f131cb5e8dc4392d21054c4ef938c0fe63fb918087f6fb97e1baac`  
		Last Modified: Wed, 23 Apr 2025 19:55:40 GMT  
		Size: 155.9 MB (155928793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d78c24fd342c2421f88bbd6e10ba6c49d434950e593aa51183aa48b9a21517`  
		Last Modified: Wed, 23 Apr 2025 19:59:59 GMT  
		Size: 69.5 MB (69529193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765357bb648f5c72e442eca2b58b4dd125144fff84b5e5488a0988f3704b5be1`  
		Last Modified: Wed, 23 Apr 2025 19:59:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eb3c3a752fc570c690cf7436332dad79d85fc45d289a5012cb61449d14bbb4`  
		Last Modified: Wed, 23 Apr 2025 19:59:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:360d06d473f46e29a87fbddbd5ad926534054795df6e1994a4a75ba46b2a373d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7232040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c320385459be7298e3d410ce1836a24e38c363fe91d633d382185d975b5469d`

```dockerfile
```

-	Layers:
	-	`sha256:b28be853ef6d6c08d2b49eeb14cb1e9876439eaa8ccd3aa54c8b18ce940ce127`  
		Last Modified: Wed, 23 Apr 2025 19:59:58 GMT  
		Size: 7.2 MB (7215402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:344c5c1df8827020fb616a8a66f3a946ed8936f19ac70cb12560920e4fb68233`  
		Last Modified: Wed, 23 Apr 2025 19:59:57 GMT  
		Size: 16.6 KB (16638 bytes)  
		MIME: application/vnd.in-toto+json
