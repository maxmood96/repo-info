## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:74d3bda6f6d4f2baab5a774fcbe3a261d1c3b39ba4291de93bff21a22b4618a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:a4e86e7e963bb140193bce61999ab60873b194920e6f3f2677c4dd1ff1897114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203651617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c825252fdd90bc45d8d5a8136d843d8abc925f293d6358d0b36d8d119a9521c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6501625c0bd93c3a9e7bdafec2b1df8d65ee819572e7bb6e337314ab31718ce`  
		Last Modified: Thu, 11 Sep 2025 16:55:12 GMT  
		Size: 1.5 MB (1450049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cd794a5e418d61cd9f0391f9aa128310c0ef64a7a804c3fddc9453c8e60e54`  
		Last Modified: Thu, 11 Sep 2025 16:55:28 GMT  
		Size: 172.7 MB (172664633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:8d8ed0552d583b4c47cd794b3b7fe65d04cb032ef7a0c5023219eb6e2848b14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3096502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0764f247578177811c8299f3f381aaf4c9a6d66ed8078a57a6bb4ca8f99276a`

```dockerfile
```

-	Layers:
	-	`sha256:bc327b38491b257672e0a4502977afe6cc3e8c379e51835b07374cda9a672a22`  
		Last Modified: Thu, 11 Sep 2025 17:01:37 GMT  
		Size: 3.1 MB (3083862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d93adadbac258a4a779929cc35c438bac6094a62a49528fa32beab5441051d`  
		Last Modified: Thu, 11 Sep 2025 17:01:38 GMT  
		Size: 12.6 KB (12640 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:08a8566ccfe4418a3fb255c8bf80d75d075ff4fa57edf1dcd626344367ee0db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209792835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7105fecb952660c84a56ed6369e637166001c98b86c9d5729c71d12bfd168518`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a9f118ca1f1cbf4058ca82bc7edc4791643f5aab1e787697cb7e9c745ab8b`  
		Last Modified: Thu, 11 Sep 2025 19:08:09 GMT  
		Size: 173.8 MB (173813396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:2ad0c9a971f6f7cffe9535a8e552aa37f93e4d387a83315e750340fba77c10e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d7b10107d12da4e11d5eccc49ed51187b4c08568a23257eb81c836508a31bb`

```dockerfile
```

-	Layers:
	-	`sha256:d73775d92e2134667c0aff4df85c2160daebc74a5b80c55cd05bc824438657de`  
		Last Modified: Thu, 11 Sep 2025 17:01:43 GMT  
		Size: 3.1 MB (3069811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d985f7e2e6540354f101f0ac3e9c767e6d383caa0f8d32a8c2befb77f6af1dfb`  
		Last Modified: Thu, 11 Sep 2025 17:01:43 GMT  
		Size: 12.7 KB (12675 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:df015a580d51c21d085a256fdbbca654ebed500e98dcb9f4d4b50fcb086578a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.1 MB (192092404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1171e56899eedb16c53b5d5ea649d0cc709f30f2d14c6e33dd508dcb16598aa6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:41 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:42 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Tue, 19 Aug 2025 17:21:42 GMT
CMD ["/bin/bash"]
# Thu, 11 Sep 2025 07:18:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 11 Sep 2025 07:18:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_VERSION=8.0.8.51
# Thu, 11 Sep 2025 07:18:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 11 Sep 2025 07:18:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b95b4dad0cf791eac4470394de71d0a10e6de0edfef58b1a82a54a4246b113`  
		Last Modified: Thu, 11 Sep 2025 18:09:36 GMT  
		Size: 162.6 MB (162632978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sdk` - unknown; unknown

```console
$ docker pull ibmjava@sha256:9a29e52165ffe924b8a4b096073fcc93b18c0267fba859fa8365bc05561df20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2769819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b84372ba8dabbe00c434d3759fa6b1f69738b55448e441e7e3a9ce34ce98afb`

```dockerfile
```

-	Layers:
	-	`sha256:f15d35e9681977cabbff2d13b7143d3711edb2591c8307bec77e60decaeaf5aa`  
		Last Modified: Thu, 11 Sep 2025 17:01:48 GMT  
		Size: 2.8 MB (2757178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8212a42d609e6b91efa2b219c2f30e17ed3e3f8f08b9a1f1fc74f297a8e502`  
		Last Modified: Thu, 11 Sep 2025 17:01:49 GMT  
		Size: 12.6 KB (12641 bytes)  
		MIME: application/vnd.in-toto+json
