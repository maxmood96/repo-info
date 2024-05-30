## `clojure:tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:233590ee502ef1a8450e93963289a30322a648df89d08e4c5ef18cf05b5f12f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:bac45d0a044b1670bbe3d94b9c579c6fea5de126f14d2463e95e54a1e77fe7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288368853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fd8f67b0ed19c0053fbb2b751f1687611e1ceeb15b51cc53a1ccda7d979e48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ec5bf63fafdf5e24329b64cbd02cd87c8cdd830df701e1248f13b954f97e5`  
		Last Modified: Wed, 29 May 2024 19:58:32 GMT  
		Size: 158.5 MB (158497942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63234e11240fe80e0bd66337ec34af7eee9866a18ee3334d1b0aaacaa0dbebc`  
		Last Modified: Wed, 29 May 2024 19:58:30 GMT  
		Size: 80.3 MB (80293473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51af9a9da4b0af1cf6c27d27fb8a8588cce4ca9dfffdf69c17c0f40f99427b39`  
		Last Modified: Wed, 29 May 2024 19:58:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a7eb2c2f42932a748187f0be6b48d89b9906d720269e4931bc4f4c67e1b03a`  
		Last Modified: Wed, 29 May 2024 19:58:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:dc2d2955afb2f763bc6d0fbd63f4d3a7a88dfbadd59ad60b17887574c6f4686c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acecf70b0c2de0a55266364fb5f1cc73d77ecb9a2e5708f3f71b6817ac7c6e1f`

```dockerfile
```

-	Layers:
	-	`sha256:dfbc6b4d88ddbcdb623278cac6ea4deb052b7dcb458d198b3617b94445891771`  
		Last Modified: Wed, 29 May 2024 19:58:28 GMT  
		Size: 7.0 MB (6962677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d05b3b0be9f239c1fb31b49552f5ecfadebf2d8649c564786c86978b507d79`  
		Last Modified: Wed, 29 May 2024 19:58:27 GMT  
		Size: 17.4 KB (17390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19e2c2f7c827aa799f7f3f883f5556d2adade868d5b93bdfb4f601143c475b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286325087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d76eaadf46d82647ca1a47519c181dca3f5e33b63e6e1df88ec2307145cff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8cf129a6a2c7c80a986dd2af0048d3bb592294757df25be757b347870821dd`  
		Last Modified: Wed, 29 May 2024 20:23:00 GMT  
		Size: 156.7 MB (156665610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170b17dcdeadde8a34733c4295ca704bcb78b3c801d6377e552c9648c98b89e4`  
		Last Modified: Wed, 29 May 2024 23:11:01 GMT  
		Size: 80.0 MB (80045041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59cd1ffd0d0c27a432fbbecb38956c5636c3226ba0af6a8e25beb560c3bdc18`  
		Last Modified: Wed, 29 May 2024 23:10:59 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dee76091eb9397daa40d2818c3c108b22fc8aa7ae911fed306e19f5598c6e3`  
		Last Modified: Wed, 29 May 2024 23:10:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:f079d39208b2b488283dd824333b1d3b2846e6540a5cb7520190af50663bc8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6987134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d3c6bdbfa6eb2a921e50fd881c6bbbd97450cd03b28e9786a07511ac54fc7d`

```dockerfile
```

-	Layers:
	-	`sha256:806f8dc099dbb8f66d1448f6e8d5f660b2ddddedbc294127f4b02934969a018f`  
		Last Modified: Wed, 29 May 2024 23:10:59 GMT  
		Size: 7.0 MB (6969136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42af80b09aa1d171ea63c29a8adbb98987d36cec8332739dc640ccd6af9c15d`  
		Last Modified: Wed, 29 May 2024 23:10:58 GMT  
		Size: 18.0 KB (17998 bytes)  
		MIME: application/vnd.in-toto+json
