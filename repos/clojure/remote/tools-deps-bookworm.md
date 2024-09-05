## `clojure:tools-deps-bookworm`

```console
$ docker pull clojure@sha256:bd8f585a012a8e449f56701618478d99e35a3a63d4b24e29f9c35ca17f7e8bcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm` - linux; amd64

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

### `clojure:tools-deps-bookworm` - unknown; unknown

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

### `clojure:tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:55872abbe0d7f005bd075238d7ca5a0d3de2e9c081f78d8d2f2d2cd6c67cb00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286534231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fa53cf4cddb67ed2723607192ca7c0cda270f782fb31bef95dc84eb365024c`
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
	-	`sha256:432a3dfe48f41ad044efed0a39ddc56c9ff96bfad23f28032c6b72e9206318e9`  
		Last Modified: Sat, 17 Aug 2024 05:49:36 GMT  
		Size: 156.7 MB (156746222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301280ba1adf4535e95ff22a9db87b681705d89c4c0cdd26e2078423d991a907`  
		Last Modified: Sat, 17 Aug 2024 06:27:44 GMT  
		Size: 80.2 MB (80198376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64123b6e5cb94e7d4c6b74dae2b5df37e555030f3c1915d1f418a848ca2e6b8f`  
		Last Modified: Sat, 17 Aug 2024 06:27:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088c75c54295a45aa171276ab10a28dca4194302447e81da3a4e02d5dc40478f`  
		Last Modified: Sat, 17 Aug 2024 06:27:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:81f4c41d3d607a95ecb6b7dd2bb52a756ad2eae13e51551b18f83e03a2f80af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0619a6c74350a0f09082f9321e81eda04c12f773e285bd6e89fcffdbce3b9dfa`

```dockerfile
```

-	Layers:
	-	`sha256:dc61055538599077ad8d23490b14286400aba889ba1ca736dd7bb1295fb1299f`  
		Last Modified: Sat, 24 Aug 2024 00:06:22 GMT  
		Size: 7.0 MB (7008555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c910d48e0fefedd85389bf860deb96918d9f4b2b101a16c0cb4d67fb422332e5`  
		Last Modified: Sat, 24 Aug 2024 00:06:21 GMT  
		Size: 18.0 KB (18047 bytes)  
		MIME: application/vnd.in-toto+json
