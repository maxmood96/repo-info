## `clojure:tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:2f0ef52ee605788e34120fd3a4df9fd0c17346a49f507b79d9edd7d91a592e4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c2255e46dc9775919fae848ee41e66893bdf7cfc6022e06647d0e6bbb50c0ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248948947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb917a0e7a61f0aacda71421ff6e9ad377a4aace5ad964c1927b7f7fa6f8e8c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59e3920ef71fff1f59719fb0689e5d52531eeef7e6f6d7101ae7e161c2be8e2`  
		Last Modified: Sat, 12 Oct 2024 00:54:03 GMT  
		Size: 158.6 MB (158579253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579bd8972825a76a15c7708b3befe8c0cf5fcb80dcd12d5ee04fc5f2b62729df`  
		Last Modified: Sat, 12 Oct 2024 00:54:02 GMT  
		Size: 58.9 MB (58940053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2fef6b0611e334e3304468a58cc6ec037cda9bde14b15e51fb5e084f752ac4`  
		Last Modified: Sat, 12 Oct 2024 00:54:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc26ea0f36ab8461b295f4d0f14a8d24af5f5b3d40105e19f6482c7a8c13d219`  
		Last Modified: Sat, 12 Oct 2024 00:54:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:60922256dde1b62b89ccc513543ce1a25e800974edf918cb5d77f758eda3680a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25196ca46f4a1a1918a3fb57e53b5ae898f9811e529672ef59e903b3db0334e`

```dockerfile
```

-	Layers:
	-	`sha256:459ee6aba5431276e8bf053ed2ee2b5b02e347678d7d661a8b868c48fa206952`  
		Last Modified: Sat, 12 Oct 2024 00:54:01 GMT  
		Size: 5.1 MB (5103282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15201ac2f3ba81ae23b3a8876e0bb0c0f3695e277a2831d4feaad891b56019c`  
		Last Modified: Sat, 12 Oct 2024 00:54:01 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d34c829f22128238645e24bea29bd37b7e778b6630f1b31802689e0eae98afd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245895701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34b34d17d8144a891a41380ae3208fa87481fd39207aa16aa9feace05b7c572`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d8e0685c3f988ae916e88e6ecba4356a7500cf551218d3a0ac32b094d00f8e`  
		Last Modified: Sat, 12 Oct 2024 01:24:50 GMT  
		Size: 156.7 MB (156746190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa4d42c0e6f58e3b715798bc77e58a11482e5e6c3d20d75a33fd885d5c90b5b`  
		Last Modified: Sat, 12 Oct 2024 01:29:49 GMT  
		Size: 59.1 MB (59073308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d616670c805f6dc23a58cab0f113882ff5a71339cc675e6c02d3a4159969e4`  
		Last Modified: Sat, 12 Oct 2024 01:29:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecdee94cc1f5280177485e23e6103e73119383bc41577f589ceb74dd2ae9df6`  
		Last Modified: Sat, 12 Oct 2024 01:29:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69f317c4cfdc0fc46973327c291776d50da8f3c0f7559c156027492df82eeea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7aa9f8aefd798d9b55f7d70885110e32c6084b0c014d8ce03baf8e8026a565f`

```dockerfile
```

-	Layers:
	-	`sha256:c630cd11c74b877475ba744d81f2ebab6c2aa21a81add94b63e27fde5800e52a`  
		Last Modified: Sat, 12 Oct 2024 01:29:48 GMT  
		Size: 5.1 MB (5109043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a67d55178384d8a75804ab800c786d6babf9df5caedaa6e29519406ed7c390`  
		Last Modified: Sat, 12 Oct 2024 01:29:47 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json
