## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:e9c21e6c8995659b44e15a6d0c55d077b2ba536d8170a77f1483eab5b473c7ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7dab1e3040a4ae7797d8819df8782b89483b0ebf29bf32cee8ded85a3ec744cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248948880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc8ac31ee224a429d73b3ecc8aa0f27be4577ed1055598cad08e5efdf0243a2`
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
	-	`sha256:e65b194e8194b90f843687f6c6c8134ce7895d024364fe77ce729a19f434495c`  
		Last Modified: Wed, 16 Oct 2024 16:13:30 GMT  
		Size: 158.6 MB (158579314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce78d84af1511eedd567083b53b92d9396e0a36f8818165cf9ed6e692c8cdb33`  
		Last Modified: Wed, 16 Oct 2024 16:13:22 GMT  
		Size: 58.9 MB (58939920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f424003812107b11dc0ca01dd060caaeac47bc0ffa366590fb44233bc282cd56`  
		Last Modified: Wed, 16 Oct 2024 16:13:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0def6bb821c77810f354abff8e2d73a3d5495dae499accfe9988c28dbb6b1`  
		Last Modified: Wed, 16 Oct 2024 16:13:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a68b3d1382ce2f2df80b662f1912ebb980ef63617c36a83e3389636a23d87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5119529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc50f5718cb7bcc8d080aa16d75dbb159aff55817d464278cefbc39239966c0`

```dockerfile
```

-	Layers:
	-	`sha256:dbfb6534cb1e86369418de4cb00260f1c9211221406f94b476ca9dba693c44a8`  
		Last Modified: Wed, 16 Oct 2024 16:13:20 GMT  
		Size: 5.1 MB (5103282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66f1f2a30553d58bb2027ae7971341e7af6f8790c8e4e0b32d8efda60bee26de`  
		Last Modified: Wed, 16 Oct 2024 16:13:20 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5b9cd5dd286b43b6a3024b0a1e6293aff7024280fb64239fd680eb60a9a467a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065b70384458136f0db455fa4fdae8127e6d7e706bda4e35efd07eabaaf8dd7a`

```dockerfile
```

-	Layers:
	-	`sha256:a8733aabdb06387ac9c0941d43d7e8257f9a12fac68a9a372ea6487513a93cd8`  
		Last Modified: Wed, 16 Oct 2024 02:36:59 GMT  
		Size: 5.1 MB (5109043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:433132fb508e9caaa9e7d21cf0f3372a63f6090fe3311419f1d51a2949d91ac7`  
		Last Modified: Wed, 16 Oct 2024 02:36:59 GMT  
		Size: 16.4 KB (16376 bytes)  
		MIME: application/vnd.in-toto+json
