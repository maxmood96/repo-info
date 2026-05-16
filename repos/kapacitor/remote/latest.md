## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:f61630a45ec685fea67125dcfff2a1c0adb48f4e507783912f435f9c39e94505
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:21ab0cafa733815b533de71700e6144ac4b1a7667088d50cf322f303b3f25565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174503064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbf68ce343bed6b6feec26179d886e7e0ea241656472c2478f8db8ee64daca0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:46:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENV KAPACITOR_VERSION=1.8.5
# Fri, 15 May 2026 21:46:23 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:46:23 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:46:23 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:46:23 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:46:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:46:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0aeb1f8fc5f0c234e2220faa9320cdfd32528ee5a33d4b932677603206a1e8`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 7.1 MB (7106733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46159866ad82a5c777187ff50c453289ebed543b8f9f68248be6d79202aa9f4d`  
		Last Modified: Fri, 15 May 2026 21:46:41 GMT  
		Size: 51.9 MB (51915346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f3cf074a7121762bbb3538695a60b3625b8df65a296c33336433c170ffdf1d`  
		Last Modified: Fri, 15 May 2026 21:46:42 GMT  
		Size: 85.7 MB (85743781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fedcc49bf04169eda6042ca14d5a99c7bc1db25cebc554ba4a3f4f0e8170b8e`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f5a0a593fce94b8ea0fe8759d01793ee19a4ca10a238ef57851d0d51821412`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6ceb89dc0a0a4dbd4128e60d5e9f79361d95bc3b19b32f60de5526dd70ebee7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7a6f1288f18d09acc218ea06c754f5fa45c4241417833bcbfbfb753ae8cc3b`

```dockerfile
```

-	Layers:
	-	`sha256:06a3fdb6cbe0f3a9d43f449222c4a3dc5e6f789dde3ba366fe9b1518ef414ddb`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 3.7 MB (3732028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5e61e6aaaa0faa0a4a1424e949c788bb835290992273fe49911d193a945dfe`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:276a60d51dd87d293c5337310870b0dc42d499a35f9c23ea69f4c970a9c04e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165824584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435a681c29f0f50a5607588df1153c012a29c0d5e92b52ce759ffbdc9d1af154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENV KAPACITOR_VERSION=1.8.5
# Fri, 15 May 2026 21:47:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:47:29 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:47:29 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:47:29 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:47:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:47:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3443b99bfd9ba84dc508ac1e64f30df03b505f391957f7bb18008ddaa77c1`  
		Last Modified: Fri, 15 May 2026 21:11:07 GMT  
		Size: 7.1 MB (7061756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca325b534f8e5bf28c4acc9719dbc6ebf82c802117c93c633569c5bc7c73dc14`  
		Last Modified: Fri, 15 May 2026 21:47:49 GMT  
		Size: 51.0 MB (50992580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ae8658efa64ea5aa54a5dc2789327c0ef6a3b926e75c4d838856b23139b000`  
		Last Modified: Fri, 15 May 2026 21:47:49 GMT  
		Size: 80.2 MB (80163104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3d874ec011cb8cf46d4b10a5f672a7a09fb3bd7a5f56da0821837c8e0d79d3`  
		Last Modified: Fri, 15 May 2026 21:47:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9eac2e987f716e7e99e84c7492d00a16507c4b3c6e175d62034974ea4266d`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6021f0c0b5eaf82a9a51acf8cdbe31f693a9ad4313675794cb57305d8bd36296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6a004b36323e9dc276d74ca38239db3033b03f2a2e1aa249a8a7e521af7170`

```dockerfile
```

-	Layers:
	-	`sha256:a43558c11e4caf94a2a8e22556c366dd33713e9ce886b76d3eeb7bcedb64c2e0`  
		Last Modified: Fri, 15 May 2026 21:47:47 GMT  
		Size: 3.7 MB (3731502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4d7e727e2fb7205e7d775288c96a70868edd027d1b9892bf49cb13401c0c8a`  
		Last Modified: Fri, 15 May 2026 21:47:46 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
