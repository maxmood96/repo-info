## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:e6f213505ca2b41e02a7de5259a51b581b61f89625d2bf45c2dc05d1495ddd3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ce34d8746733ac878bbdfbc2f364b7f1fbc8b435368f0f2232a73202a45da486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269345566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd36928576523f13b9e64a2643fa0db30e90c4f5acf1c38a517f4f3f316d377`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1873ef51bdcca3e237da7aa54aae4c5b7d30f27914dabb6175706483a6700fd3`  
		Last Modified: Wed, 04 Sep 2024 23:08:02 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff13b0ce95c49ad851943e7124b802d110aebd430ad2e0d1e002405af1b69f88`  
		Last Modified: Wed, 04 Sep 2024 23:08:01 GMT  
		Size: 69.1 MB (69096659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fa23c072381a0aee799dd09fc4f2d69cad833ad4cfdf2f4c1ca91feaf2b2c`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e48fa34fed5549c819464863c8bfe97ff354124f98c7acca1b60cda90289794`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c33e3579f8f7d1dd4293df9c4082c1e675a069a4ab5fb023618f65d93b9fa0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7f032a62d7980f77e70e04f972f2249ee4745c609ad98c5386d8d0d3b0634b`

```dockerfile
```

-	Layers:
	-	`sha256:d2fd2232d8f9458e58fceb94e5a4391cf99e84c0de39cb94ea7ea10d2fc0b0f3`  
		Last Modified: Wed, 04 Sep 2024 23:07:59 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f950cb9b6bf443a5280d9b6ea1880db6cd7c4fece389deb6dbdce091cf40f39e`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1077efeda1da392440ecb06f9b4edae4280c4e01df679b16818fb9659eb82eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266784013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc823c498554938d56f1521d156722db4819f2a3bcf8e817b20edfa9bc70e434`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfa56dc6386c5135566e66fb0e37350a34766eea8404060c807317e8b8b4019`  
		Last Modified: Sat, 24 Aug 2024 00:00:01 GMT  
		Size: 144.0 MB (143959466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77de5672ee820736047df308a9eba3596a6159436936dd2356b8732ab1c0e45b`  
		Last Modified: Sat, 24 Aug 2024 00:03:14 GMT  
		Size: 69.1 MB (69093587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718ece921a9af34650d847f8fc04461b4f6e83fce2078314635587df41689493`  
		Last Modified: Sat, 24 Aug 2024 00:03:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e6b667b6a5a6ead629cf66430cf2e56bc628d1fb2b66f2d23a15f4abff9c0`  
		Last Modified: Sat, 24 Aug 2024 00:03:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3b5c24304d061aae0b730d27947c1ce01012d414fcf57956b1bc3905b6e573f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec451cfb916fdd649902cd733e37f6ab1a1cf7c964259e5e1e44e716d5eef77`

```dockerfile
```

-	Layers:
	-	`sha256:ec37dc7da408df36be4a0345e1120f90ed30edaf36b226ffd28bfb39e7886184`  
		Last Modified: Sat, 24 Aug 2024 00:03:13 GMT  
		Size: 7.0 MB (7046066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c00315735db93026c8e8ed0aaa6af03b23ca5b57d5f775cf9d21166474a3fb35`  
		Last Modified: Sat, 24 Aug 2024 00:03:12 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
