## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:58ad87013109f347b0fa77a3e27e45bcd0883a51e6b0e2b384e96dcd7906c108
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:c69aa67a17801a91b2125e2370bbb42feb3fa44e4c8092c42f0abf02617ff7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288603198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9f97195c5133da34bf6538ace83095d5f6f4fb5f880abfac13fb21b517d369`
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
	-	`sha256:b5b9192a7719f96730ead0b6c1977f0e4867c0452c645e0fb8a6ce98226c6f3a`  
		Last Modified: Wed, 04 Sep 2024 23:08:06 GMT  
		Size: 158.6 MB (158579245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042e669bb67e336645d5daffca958dbfa8897899c62be04dc7d73ce67aae11fb`  
		Last Modified: Wed, 04 Sep 2024 23:08:05 GMT  
		Size: 80.5 MB (80466208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22f54530147b6e7b6948d59f827876f7dfa51899ea675f974bef9ba9ba681b4`  
		Last Modified: Wed, 04 Sep 2024 23:08:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8852d5f5089b68fd781abd2652d797478bc939123545e12dd889d4edde226114`  
		Last Modified: Wed, 04 Sep 2024 23:08:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8d9417c249415806ca6b2cbe82d01a837139c0555218349174bd8d0de321faa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7018919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be256b9726f34a74ee39440e086b995379d676786185c3207602d0f26bae71a5`

```dockerfile
```

-	Layers:
	-	`sha256:0995334ac7791f05a325e7703fdd1e8386ebbb460907b1eb3352357f9386b8df`  
		Last Modified: Wed, 04 Sep 2024 23:08:03 GMT  
		Size: 7.0 MB (7001481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2282a627350b9c16f306efe3d5a6b59b5c1ca4e3a2ae8379a92cc345c852a41c`  
		Last Modified: Wed, 04 Sep 2024 23:08:02 GMT  
		Size: 17.4 KB (17438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4eea9aa939af272c6f951e0535bcc38b0b69d8f1ebb063982b20d9379a16d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286542262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefbc285dcdd5f27bbdfb570b8c9c738b99adc7491e068fc4821a67defce2619`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
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
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309b46fa0b162a627a54ecab3826334bb069c39d9832f52c5f8bd1d7b58c992c`  
		Last Modified: Thu, 05 Sep 2024 07:46:58 GMT  
		Size: 156.7 MB (156746214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4318eaaae1d9bc6ef0bf25b56b125ba4fa45953cdee761199a0311995801422`  
		Last Modified: Thu, 05 Sep 2024 08:12:15 GMT  
		Size: 80.2 MB (80209380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfcbf76c94aed96835eefaa38e24dabcca9c49c94e721b2469be61833475a4b`  
		Last Modified: Thu, 05 Sep 2024 08:12:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98a2a11c5d9b4ce6cf7f46d8d17277f96962e6ae18e820542c51d19028896d`  
		Last Modified: Thu, 05 Sep 2024 08:12:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:3f10d059f19d6154b8972d290d6da21aa79271baece85b4402c399b759751161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7025987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8406a2a2c92da31d0cc2b436f0d9603125765ad2049fb08511fc32a189716a4d`

```dockerfile
```

-	Layers:
	-	`sha256:637a550ea9d1e3b33a6bc3584131753c35fcb4602c6fac65185a2f8963e7ff92`  
		Last Modified: Thu, 05 Sep 2024 08:12:14 GMT  
		Size: 7.0 MB (7007940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00670bee563417a14c095f108899dc678482d9b0b12668e45153b41ccc2ff459`  
		Last Modified: Thu, 05 Sep 2024 08:12:13 GMT  
		Size: 18.0 KB (18047 bytes)  
		MIME: application/vnd.in-toto+json
