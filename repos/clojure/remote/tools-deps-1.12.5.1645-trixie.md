## `clojure:tools-deps-1.12.5.1645-trixie`

```console
$ docker pull clojure@sha256:2a5edab268074eff957d99e515a12b5136b2079a604867904c36ea0ef2cc362f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fcdc53557b9c221fa8c75c789e8b7c7d96a322efa0cdbca8b1fd28271357e574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227481488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34913f2d5a9e244459b8731bc8b68fd7de1e8cb479309d64aee2eb43ecadd19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:10 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012b166ac5adafce01ad3e58a07b9d3c7fe050f19bd742b5c9e2299c775bc0ac`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 92.6 MB (92574589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385801ca07d21c19cb2c6e80fae8b86e47aef62926733a99a77e4fee511b3511`  
		Last Modified: Fri, 15 May 2026 20:16:52 GMT  
		Size: 85.6 MB (85603537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39802efcd3c5c47d45ac0891763d03e5193246fa35c94baeee014a19d1fc249`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b09360e82c7bd08e3d823e26e4413a296e5d97a41ceba53c8925265f17b87b`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4975f87102740f5cc943c4cd6c6581098df7f99a2481805e9542f335788228ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d755d6d5555478cc76157ce8b780ef94c5bb2cc4dfd8241318180ec2b0d1a49`

```dockerfile
```

-	Layers:
	-	`sha256:9a16e0fd8d2bc2d9458c6a2fad397df1782376c43cc6e164042b51768eba0f9d`  
		Last Modified: Fri, 15 May 2026 20:16:45 GMT  
		Size: 7.4 MB (7439444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806d56aa3fcd04e6675ee15e1cb6616811889650ecd2b409a0397e508fc9bdcd`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ccd4d8e29d01acd13c9a9a9cf7be7c3c77ca2898380660705f4d0cb0b38083f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226628154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de11384bf173ef60dd838e3f15559b46b8718b1031d1552ffe89b716e56015d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:13 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:13 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a585bc135b4a7328b968a7e3ea6be7e3de0a30a835beb50e7136cf297de6c3`  
		Last Modified: Fri, 15 May 2026 20:16:55 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb20b1ad8544deccfd1f8733615fb5c357c6823df48ffc40d4376e989a6fc4a6`  
		Last Modified: Fri, 15 May 2026 20:16:55 GMT  
		Size: 85.4 MB (85415413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442bcfc4e41d9c84dc6aced5ee267ec87725aafcb24a6408ff0da6ae2e309932`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859fa332166d6ed8f8fb37c654557551904985c8f1db4b208f5b4bea38539817`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:607766a76f55611355285b4372dd8cefb2285b8b550790e1f985117312266924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7463206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eeae80a4c1b72e73387cfc2f0ca726bf15c62de5c85ea32b08df4a82d19c764`

```dockerfile
```

-	Layers:
	-	`sha256:d27d6f7b7dd1bad2a8ac96227fff63fffcd47ddc993cc153e93632a04b0efb75`  
		Last Modified: Fri, 15 May 2026 20:16:50 GMT  
		Size: 7.4 MB (7446495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8773b35ad58d1bc82c7b3b3f1e9a1689aa1b9c1c5c4c08f590c2bf89eb2b197d`  
		Last Modified: Fri, 15 May 2026 20:16:49 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json
