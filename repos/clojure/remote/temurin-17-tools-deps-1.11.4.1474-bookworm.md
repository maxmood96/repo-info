## `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm`

```console
$ docker pull clojure@sha256:0643b385fcf0c337c1cb641974059daed6bff9153bdddd615e4e1fc8c968cebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6b1204a7315ec469f4c6d7b013204e99447199866dd8f2d308d15c44f89da1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275190473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9bde59a2dcb25cdce0d8ac621bee964493b05df471c970d11fc26f0c50d86b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1873ef51bdcca3e237da7aa54aae4c5b7d30f27914dabb6175706483a6700fd3`  
		Last Modified: Wed, 04 Sep 2024 23:08:02 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fb0e7f5fc52606fc523a36076991441776adb7b44254d1de81564422ca6e75`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 80.5 MB (80466195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39178358280018db0a06aa31087ba633c6147d99337a95ff2590698b7679f26`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43577a486484f9ba7efa2643dddea35f7cd4cd94941fbdb0f6fb62381160f8e2`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fe98999baa85b840ae2c119bc75738277fbb342c29b1bcc714759793975686e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7014911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3653511bc407ac3162ecf77a351fa25a97096571a683bec7fef828029ff7b604`

```dockerfile
```

-	Layers:
	-	`sha256:02de887ba461d295e983edf0f542011fc6ee3acc0c767cab6bd25d732dd2043f`  
		Last Modified: Wed, 04 Sep 2024 23:08:03 GMT  
		Size: 7.0 MB (6999471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b05bf7eb735b29fa0cd86c821b74808b6e58974303b436e1f75b91f03ce8b22`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ebb91074f6d080dcc34ca353bc9b450964287929217631e9c0f1d0a06324adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273747318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3053d42a193ef0519b65597ce557b652541a10ebe51d7c3f468744805a02386f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea87b501a62dd02775c9e05493af6f0f62d3ad09f4f5edf7aea8f5d4fa7970`  
		Last Modified: Fri, 23 Aug 2024 23:58:09 GMT  
		Size: 144.0 MB (143959472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a77a671f03844fa7583fe63f78ca6178a7169f3cda410335d67deecd486271`  
		Last Modified: Sat, 24 Aug 2024 00:01:43 GMT  
		Size: 80.2 MB (80198211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757454b7bf8a2d4e7e7b6630e855c8bd13cf4e5da8428d9d05c736070a360d7c`  
		Last Modified: Sat, 24 Aug 2024 00:01:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78669f5384dc9bd54078399ca0feb91290f3b81dc497265ae836cc72ccd6f62`  
		Last Modified: Sat, 24 Aug 2024 00:01:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:75741c3bbb4c4b737509ccfa90f5a9656ff8435452962c6a4adce89814c97539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbcdf22840ca9696efd2ef7dc55cc59682616f6c2d08dc3321ed5dea27be085`

```dockerfile
```

-	Layers:
	-	`sha256:8a6ac6584226c3adb93a7d47c008326b9ad6168aa279f5e123a71730b9b3694b`  
		Last Modified: Sat, 24 Aug 2024 00:01:42 GMT  
		Size: 7.0 MB (7006473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec316fd075fbbd43f12f56f83e959231a730c150c7a2c0fb37b2e807f86d6b4`  
		Last Modified: Sat, 24 Aug 2024 00:01:41 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
