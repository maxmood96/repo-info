## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:51e474626b6b81cb67d59fb158255e275b9e147fe7d716bf59d87c11c490973a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:59ff9fb550215e84b3e394fad0d0f0ae8e3eef2ba7ef2d78c96fcac70ca82e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280778521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e262f19910b2a932cc917001a43bf7216890b452a5b51f5a614ae7823dc79a78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd86af4d1b05b1024b612c413f592bf053601f5b3d6d0f31d9842e33929b116`  
		Last Modified: Mon, 28 Apr 2025 22:08:08 GMT  
		Size: 157.6 MB (157634490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556f5c0e46f16e554d9766549a4e0fbfb3c625a36bb1ff4ce624665f5735ee81`  
		Last Modified: Mon, 28 Apr 2025 22:08:07 GMT  
		Size: 69.4 MB (69395250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1251b964e9796522eae64ee2d591b7ec132fc3f105f36e9010c3f3cecc3bf083`  
		Last Modified: Mon, 28 Apr 2025 22:08:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce1c5f25602ee233f19989ce58aac8ada729dc5f78464711e47bf8e0a2197a`  
		Last Modified: Mon, 28 Apr 2025 22:08:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:30cc313e51e86b6b4442785df13ae966f5b96b3dad861492b430a1ed7b2294d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7226829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a34816568e06373d0755d17e75823146f0261763f81c18e1eddab106a63d7ef`

```dockerfile
```

-	Layers:
	-	`sha256:591615c195268730dd69372ea004dad60dcad8904f59070e516574e36a13362d`  
		Last Modified: Mon, 28 Apr 2025 22:08:06 GMT  
		Size: 7.2 MB (7210333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1ceffc6ecca3bb9cf2b4544997715b2da2525d0196e5ac034c3b6ca3624400f`  
		Last Modified: Mon, 28 Apr 2025 22:08:06 GMT  
		Size: 16.5 KB (16496 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

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

### `clojure:tools-deps-bullseye` - unknown; unknown

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
