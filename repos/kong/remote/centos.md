## `kong:centos`

```console
$ docker pull kong@sha256:796bde8b61581c315bbfdf3c85e9002599dc630c6fbb456c8bbf9ec5aa2c12cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:5e129dca95cbb055cdaaa9806966569be196446d3b38122a01991a1245e1c1fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127222587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ff1d4be6c902aabe1ad9a93e37eac121f1781af332682e2826cb27087f357d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 05 May 2020 21:54:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 May 2020 21:54:26 GMT
ARG ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
ENV ASSET=ce
# Tue, 05 May 2020 21:54:27 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Fri, 10 Jul 2020 20:23:32 GMT
ARG KONG_VERSION=2.0.5
# Fri, 10 Jul 2020 20:23:32 GMT
ENV KONG_VERSION=2.0.5
# Fri, 10 Jul 2020 20:23:33 GMT
ARG KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Fri, 10 Jul 2020 20:23:33 GMT
ENV KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Fri, 10 Jul 2020 20:24:05 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Tue, 14 Jul 2020 20:21:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 14 Jul 2020 20:21:20 GMT
USER kong
# Tue, 14 Jul 2020 20:21:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jul 2020 20:21:21 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jul 2020 20:21:21 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jul 2020 20:21:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce7701dd3817fcacdc04d8abfd7cd6ea61fe7f4d909903260a2ebe43fce007f`  
		Last Modified: Tue, 05 May 2020 22:02:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e839438e3b2588088e4bb0885546faeba1afe1d70b47fd88048e9d0c70ae370`  
		Last Modified: Fri, 10 Jul 2020 20:25:43 GMT  
		Size: 51.3 MB (51341586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9126f205ac0dfa5d13b956c46b11ff4a8f1b45f444a6d30d7d070dbbc3f882`  
		Last Modified: Tue, 14 Jul 2020 20:22:29 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
