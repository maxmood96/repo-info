## `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye`

```console
$ docker pull clojure@sha256:e8e6f1a106ac3df0364c053515ced21ab2404e32a2aa0fc055bc811ef557d0db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ce72db1552fc21548cf198368fe502f75e3d3a627859361e6688b80ecbf18cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215601304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d7f5f30f4e2292811d4d546970202b8be6b6644df01bb2df66a1a1fcac579d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:36:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:35 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:48 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e62a36a22bb9aa2ea557b0a0699b0af1841dfe29918d0604f59f347c22e1bc`  
		Last Modified: Mon, 09 Mar 2026 20:37:08 GMT  
		Size: 92.3 MB (92256329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543b8d6465ed8facbcd48291aeb123ae5b2ecfa1da84138d29e4dd4841d5e9b`  
		Last Modified: Mon, 09 Mar 2026 20:37:08 GMT  
		Size: 69.6 MB (69587501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f76390c2d9981569316759cd54dc535c462ac6bce3aa720bf60508a83ac1e8`  
		Last Modified: Mon, 09 Mar 2026 20:37:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b118aff9f75270b1f10160155fb128db2e5a425e10c7fa67015db0dc1dd8c46`  
		Last Modified: Mon, 09 Mar 2026 20:37:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f89668a7b1bd9d78e12880e1c09fc123456a417d93ac32d012afd476f2546f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7393797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6253dadc1f2252912a5bcfb5646e8eb9a654a4b1022d9b70cad1f6c0c5e210af`

```dockerfile
```

-	Layers:
	-	`sha256:010d5de9d319dd540f5b58e246fbb31fe099f1daa6e536a8782d102cae28f306`  
		Last Modified: Mon, 09 Mar 2026 20:37:05 GMT  
		Size: 7.4 MB (7377351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415f2e88b74538389ea939efc2784df10eeaa6c1adc8a98d028e1328afaba483`  
		Last Modified: Mon, 09 Mar 2026 20:37:04 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfaa3c780908c24684460344d09ce7b51f5466eaa5f25fbb41ca0dba3f8e8666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213276249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c434c70ce31cd79560de6315c52d92622339f5cc4374d6e4a477424dcdd06f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:36:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:36 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:50 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97968987b8353da33f2d5a62f5f2eb261b4045060e12ce3b19fce16e3679e9f3`  
		Last Modified: Mon, 09 Mar 2026 20:37:12 GMT  
		Size: 91.3 MB (91288266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a014703434127f9f2ffadd046c4e16f27e365b542fefd41f6207ac0dc9a2072`  
		Last Modified: Mon, 09 Mar 2026 20:37:11 GMT  
		Size: 69.7 MB (69728548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62dda44a5dd88cea51bba35ce1f39c3421a8bea3dce83172f9fa77fa31909bf`  
		Last Modified: Mon, 09 Mar 2026 20:37:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bc2965ddb0fae661d533bb9a10003dac684b264ef6ddfeca6d1c7b80dfa05c`  
		Last Modified: Mon, 09 Mar 2026 20:37:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:89651bea9432b5a6d4929f4af650b8108d062ce5470f9e8f96570ee964562802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0968c3b2819fd4286f4a332357272269bf6a9983a8977abee220664a42f29f2c`

```dockerfile
```

-	Layers:
	-	`sha256:df3f6b79d68a5d58f06643d3d6e9ef151b7f0e3dd07a0b29c5bdd538f4a57206`  
		Last Modified: Mon, 09 Mar 2026 20:37:09 GMT  
		Size: 7.4 MB (7382471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da5391c350504dca205a5098da7372520bc9e9db94a1a49149dedf2cca16ac1c`  
		Last Modified: Mon, 09 Mar 2026 20:37:08 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
