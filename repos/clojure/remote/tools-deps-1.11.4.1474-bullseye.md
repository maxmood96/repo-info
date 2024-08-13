## `clojure:tools-deps-1.11.4.1474-bullseye`

```console
$ docker pull clojure@sha256:74f0c8e1bb69afd1a81bb8eded5a2eea1dc6689611ac1251d9e579cc4e7018a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.4.1474-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a792421a148b6ceca6b037c715751090c6191fd61f6a35a486a8ada6bb102168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282627571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e549b90be6f3ea5bb14dc88fda9286207d943669b032724b8d44f322685aa1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefcb0c5a190958a490cac1ba5153c65e638ef7fce29c989fb77a5c937e08fa`  
		Last Modified: Tue, 13 Aug 2024 01:11:34 GMT  
		Size: 158.6 MB (158579287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9af0619c416013d2403f5ae6555d8a131ab8a60665c17a9eb8025a307ae4dd2`  
		Last Modified: Tue, 13 Aug 2024 01:11:33 GMT  
		Size: 69.0 MB (68962567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404eed446713d05d3b6bbb071595a80372c8bc43ee0955bd42f5dff6e931de16`  
		Last Modified: Tue, 13 Aug 2024 01:11:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60480b5e11243d1642666b7da410087ffe5d9867ec395a1c7ea2b612b67ee133`  
		Last Modified: Tue, 13 Aug 2024 01:11:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:329ece7ae62231b1df917c1a467de7acd2457abb23eaffbecea0b65e12e6f1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d575d4dcb672f6d544cdc10487f2181a12bc7eca962de85200e893bb521ca2b`

```dockerfile
```

-	Layers:
	-	`sha256:e69b03c7e59b72a0af7ea91a1366fe17aab220864875b42de32f8498ded5defe`  
		Last Modified: Tue, 13 Aug 2024 01:11:32 GMT  
		Size: 7.0 MB (7041030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:252f7a743f1ca28410b73f56680aa25a0f52ef4e2228ee2df56733040d5d6838`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.4.1474-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a252166d17e90491cace58dab1c08905f9759aabee7e7143d5675d05f1c585fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279570834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9c62c32ec0bde28886253c81a164a63b892483902b9d4ac02b84d14ad89c7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
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
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2430d84b3203c6622dea811cc35b3f4c6b527003ba6199fff9466c03919a6664`  
		Last Modified: Thu, 25 Jul 2024 21:17:29 GMT  
		Size: 156.7 MB (156746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de7919ffb3992856d24f9dbba9d0d7375597666da1981a524360ca1be64bb7b`  
		Last Modified: Wed, 07 Aug 2024 20:13:43 GMT  
		Size: 69.1 MB (69093622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c03a3fa8746b07e05161343de0bc81cfb7f6071f2fe1285fa12339be9aaf3f`  
		Last Modified: Wed, 07 Aug 2024 20:13:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f760325a88fe2733030309f9c3b1a575fba7c54f725f4138f3e38bef2ff46376`  
		Last Modified: Wed, 07 Aug 2024 20:13:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5680dc7ff6842aa0619f20477a242cb527dacc5fd8bc4b48f8f559955f09afba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7063452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bb16ff8d379886ea824291f6dc9ac7401a5c91fd0d76429940ab339289a5b0`

```dockerfile
```

-	Layers:
	-	`sha256:045ce639ad6e2f783cbf2062ad84e00d7e282ddba7ba360da326e7a02231cfe6`  
		Last Modified: Wed, 07 Aug 2024 20:13:39 GMT  
		Size: 7.0 MB (7046776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce720f51875ec8297994ad1fc5c9825eccec78bf67202b5dc34e00178016323`  
		Last Modified: Wed, 07 Aug 2024 20:13:39 GMT  
		Size: 16.7 KB (16676 bytes)  
		MIME: application/vnd.in-toto+json
