## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:a323fb627ccc5d9a9253efbf8c8bf44522390474039edc0b6ac65b920b00f4b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ef8e9338a1bce7c08648b548d20b898ba3919ccdc89afbc3df65bc9717270ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232526480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ed4764790575c54905694c13bb39e3c206d515a8180f97800cf7257ce644e2`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06601c15a25ce072eccd17d1468c12dfbca82e7ef4935e06017e1d4ebb47a5f9`  
		Last Modified: Thu, 05 Sep 2024 07:47:54 GMT  
		Size: 102.7 MB (102729249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96a0d66b35cb1515655cf4432cf91782a5ea060069d1f14407a9212148ea07`  
		Last Modified: Thu, 05 Sep 2024 07:51:32 GMT  
		Size: 80.2 MB (80210963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c86aad25d1ac8635d149719a743fe07e0fefe4955898d7bcf0659480223894`  
		Last Modified: Thu, 05 Sep 2024 07:51:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a304b73ada65f076a454886dca0697cde21888770a7e373b5927e234f714a56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7045735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45453f5e7f537ff3e3a962e928c10b91986eaf2b40ced0c03abcbae7c23c5329`

```dockerfile
```

-	Layers:
	-	`sha256:90460ce871166315f65c9db7066d47386bd180f6e9573b9994128cbd8ada878c`  
		Last Modified: Thu, 05 Sep 2024 07:51:30 GMT  
		Size: 7.0 MB (7031349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:828b500835413e20eaad482a52adcd76bd6ac4bc1d6fd73cc830a2c46ac7cf52`  
		Last Modified: Thu, 05 Sep 2024 07:51:29 GMT  
		Size: 14.4 KB (14386 bytes)  
		MIME: application/vnd.in-toto+json
