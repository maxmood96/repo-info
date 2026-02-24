## `clojure:temurin-21-tools-deps-1.12.4.1602`

```console
$ docker pull clojure@sha256:20f383d739617f05d96943423757e9ed520966b2c9953ea64b80fc513282e100
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; amd64

```console
$ docker pull clojure@sha256:f0af3e6bda9da2d959e152f46184b87d18c6840140de0f002180b00c3e65f28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287497309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51b15da13476fb044936425bfef9576913abb02e9a7fb865e54613cc2d4d5ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:56:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:56:10 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:56:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:56:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad774665adc6e15c1b980e49cfa7d7cb7318fd9a5fbdca51eb09f508ef493dc`  
		Last Modified: Tue, 24 Feb 2026 19:56:50 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1473eeb6f8f4c7ad4eb5e6050cad4c368724e2f3fc8248ed570884a20debd`  
		Last Modified: Tue, 24 Feb 2026 19:56:48 GMT  
		Size: 81.2 MB (81150399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2054dacaf863bc8f5435ff39072ae44d3bccac2d358151b389072bbf71b68b7`  
		Last Modified: Tue, 24 Feb 2026 19:56:45 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dd8cfcbe3cb23ae809271029a358fad4b628c6f7f60a36475f4d7710767e09`  
		Last Modified: Tue, 24 Feb 2026 19:56:45 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:82e4b7430c7e7b267ddbdf3294f8f63ce9cf7ddb937100936d8b81fa300ac48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80521997d9aee6614b45b7650dcb579ed839777c64441a49aef0130edceb4db7`

```dockerfile
```

-	Layers:
	-	`sha256:8ecaa06b20b9a65d294504018e8ba113261194400b1296e9342bf3b6ffa7c007`  
		Last Modified: Tue, 24 Feb 2026 19:56:45 GMT  
		Size: 7.4 MB (7379325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faab0197483294fbe1829b6eb68dd846a029c58539cd23c57c13a7b2afa33e98`  
		Last Modified: Tue, 24 Feb 2026 19:56:45 GMT  
		Size: 16.5 KB (16461 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c5ab26ec3d9c302cb6811b74c830eeb76a8eabae5aac329d749d444fc1278c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285645865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157b6eb5c4309077f7aaaf79663b90ddaf7db87941cc1c5f559f1327a3e05d5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:06:39 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:06:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:06:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c94e3358edcdd6ac1aef8c34bf7aa67e8a290a8492902766b457fb53e3d646`  
		Last Modified: Tue, 24 Feb 2026 20:07:18 GMT  
		Size: 156.1 MB (156133080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddb37bbccba8905eecbbce6a3cf0e0ccc35984f226e59e7d1ef90b332679f16`  
		Last Modified: Tue, 24 Feb 2026 20:07:18 GMT  
		Size: 81.1 MB (81138533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb5ce58057cc57082f4980bf902d668f5b00b2db71fe2f98c4ec68b99dbdde6`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d814278acfbfce4854ffebe946716417dbff7d90177d237e9f98cc5f109f8ae`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:5580caab6ddfafcdca21c6cb3626e76906b363b195ff757e93dd0110522d84dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446af2d95dc5e7cc3e79471e737729b4e4a83e87f2785c85436840e7284d4105`

```dockerfile
```

-	Layers:
	-	`sha256:8fe243d6b08a3aba52c2feade23e5435570fd5de05715c84ea59d73c6180c95a`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 7.4 MB (7385112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4796e4608a7156d7160c9853201779df6878d56d6ab08c5ac85a5191bfc47d96`  
		Last Modified: Tue, 24 Feb 2026 20:07:15 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; ppc64le

```console
$ docker pull clojure@sha256:bf5bf98f62b86434ce07b9e7fe219f2bb0b394948c1d7998dc9ad6d559cc4629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297292941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043b57a47cb46580e87de3caa01cba610b43a29787e833970fe4b3a0f8369c40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:34:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:34:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:34:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:34:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:34:00 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:41:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:41:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:41:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:41:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:41:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04686be48d2a894920edac0c0c6434c05a7128013df9522a975b048c103c93d`  
		Last Modified: Fri, 06 Feb 2026 00:36:06 GMT  
		Size: 158.0 MB (157977491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563ee00175dff89e342e9299356ae478e81ca394a247a61c2668e6d4d5a094a4`  
		Last Modified: Fri, 06 Feb 2026 00:41:58 GMT  
		Size: 87.0 MB (86987116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02f156a5b9e3d97c83ba351ed6f7ac043e2fa92a3e08eabc95e2f5d6eee89ce`  
		Last Modified: Fri, 06 Feb 2026 00:41:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920bf0f293d88423d1c643976512bb472450b1dd8e4f64f7c59eae0376ab4f3`  
		Last Modified: Fri, 06 Feb 2026 00:41:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:2a87b6e4dba034b8b05fafb44780748fea4bdcedefb4ec5d42aaf6ac5626e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e375320b1e2805fca907af49de17330c6c3bc4832ffe37748b09e98544d946ed`

```dockerfile
```

-	Layers:
	-	`sha256:0b325c284c37ad5a0597c298a50dce60f527c6e1096d8c9506e73fe5fb6eedff`  
		Last Modified: Tue, 17 Feb 2026 23:59:48 GMT  
		Size: 7.4 MB (7384553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23d91d9c95437c5bed2eae22570963be460cbf428d92d1d98e306fd8eb7ddc1`  
		Last Modified: Tue, 17 Feb 2026 23:59:48 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602` - linux; s390x

```console
$ docker pull clojure@sha256:54114dcbb5ecb6f57b1f81940c6db1337cf2bbc955c7e68554b664507e2d9b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274208510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c173f2c14f8e2adf7e0e19c7b645eb0c29ba5f620a9ac5e1eee190e0469afa47`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:13:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:13:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:13:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:13:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:13:12 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:13:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:13:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b838670a4f355a1ac037114110d70a67c8c7c1288cea2a0bcf49e74a0f97637`  
		Last Modified: Tue, 17 Feb 2026 22:14:43 GMT  
		Size: 147.1 MB (147105302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf40ebe17981d10019483b24c5dbf1f3edcad2edaf35b16ef338235ee9f11f53`  
		Last Modified: Tue, 17 Feb 2026 22:14:48 GMT  
		Size: 80.0 MB (79963818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af4ca1e6d77b67989dcdaa7ff5c8725e45dd4cc2abd1787e50296da24970f3a`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618432aefeca4f6d066d9cfd5d19d37e2afdbb4e7195b433fd669dc6a7897c63`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602` - unknown; unknown

```console
$ docker pull clojure@sha256:0111ec2e5ff4ab237413537b6398206d105028bcf5f2d590e104c2fb7662e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c62e9e9b1b12048fc5059fa922c873fdcfc2140cf629544048a3dfd649f000`

```dockerfile
```

-	Layers:
	-	`sha256:62de151432e669d4b69d951d723ed0653f6223c281c39de196b0b47901d50aba`  
		Last Modified: Tue, 17 Feb 2026 22:14:44 GMT  
		Size: 7.4 MB (7370644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c5213e7da4e5918712510d50473ec9e07980cbb6808d838b02478c1a09f0d5`  
		Last Modified: Tue, 17 Feb 2026 22:14:43 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
