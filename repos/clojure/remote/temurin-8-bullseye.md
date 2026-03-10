## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:a9f8e2ec354be7d625c4fb4d039bbb0a933006fa08937766150dfbbb6b949c2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:24d6fefe1c99818beb4b4aaef4ba09a440bb363a9140efda9b54402ede39669d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178514902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d06adf54c35fa6f973e3bd166526e56530b76c2be417db92e70e8363b84845`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:33:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:50 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e597dc68fb91d4f88a3d4c5f0ccf29cae15faa87f5b12750341ff558eb9726`  
		Last Modified: Mon, 09 Mar 2026 20:34:23 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea8a1d0cc37760362c7f0bb2a33afbf2840e53cbe2c86f9ec6c294ab3527093`  
		Last Modified: Mon, 09 Mar 2026 20:34:24 GMT  
		Size: 69.6 MB (69587755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d835472185a271bc7985d9c9291cb62f659d4f4f55e8cff28327522cedfe8a47`  
		Last Modified: Mon, 09 Mar 2026 20:34:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:432cb6adead8ba77cbfba91fc3cb4ec57e81dff115c704b7167e474cc2b686ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7544458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481c9d1e4647a1242738a9d4ab97f48f8ec694689f1952a756e821d79024c93f`

```dockerfile
```

-	Layers:
	-	`sha256:07b01adeebf085bec2757fe88c2e33ea1207a13e3a403cea8df4a145972ac3c7`  
		Last Modified: Mon, 09 Mar 2026 20:34:21 GMT  
		Size: 7.5 MB (7530264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddabeb9a6f615cbaba5061831d3cca5629c7b0d92234f05295e612bfc1d94f1f`  
		Last Modified: Mon, 09 Mar 2026 20:34:21 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:97e92350f50454502c6016c837ab2ab1bb98bc671f34a6bacd5c3e0b9a4f56c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176239441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f46d9e82271bd32d100947913cd0748691e3f13468bf598287d9b299e8f162`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:33:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:34 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:33:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:33:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:33:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d7fef5f3fa8587f0140c4dbbdf706e48bafa2d55861d00fd628c31ea3f5660`  
		Last Modified: Mon, 09 Mar 2026 20:34:06 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4275f97a33f7a53781c9ab039c4db4c11c85925fa4bf9549eb32b21e35fcf707`  
		Last Modified: Mon, 09 Mar 2026 20:34:06 GMT  
		Size: 69.7 MB (69728789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598412c120dfb8211c9874ba04ded009773731e0a9f19c73336b1621f22333db`  
		Last Modified: Mon, 09 Mar 2026 20:34:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:73b85b8b06d3ba0685cb18adb103db2b120f8394b6caf1256a4bbc413290a0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7550375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8c61a2a71d177192eefdb3736199d6cd6e86b6edb54fa30dc3ec1ce856f3d9`

```dockerfile
```

-	Layers:
	-	`sha256:7cf420cd10fb1c71afeb0233285a31ce57bbfcf8904855fd9fb15d7520950d33`  
		Last Modified: Mon, 09 Mar 2026 20:34:04 GMT  
		Size: 7.5 MB (7536063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ce417d28b2e72a38d55f634750ebc5b73b88ff9a07d329f9d5d8db0471835c`  
		Last Modified: Mon, 09 Mar 2026 20:34:03 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
