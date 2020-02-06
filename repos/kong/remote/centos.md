## `kong:centos`

```console
$ docker pull kong@sha256:9476ef7c71f95c8bc1374c216c319c4583afc2d9531bf00657d6de9611b1dd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:1aa80310b8c489ac3dd2923484bb918dfd405061f437abcc24a4f600ae082054
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158229085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70722a64af44bf215e518babbe891f3e8bece46ee886e1c997fbd3655e9cf6f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:32:03 GMT
LABEL maintainer=Kong Core Team <team-core@konghq.com>
# Wed, 05 Feb 2020 23:32:40 GMT
ENV KONG_VERSION=2.0.1
# Wed, 05 Feb 2020 23:32:45 GMT
RUN yum install -y -q unzip 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki
# Wed, 05 Feb 2020 23:33:01 GMT
RUN useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm 	&& yum clean all 	&& chown -R kong:0 /usr/local/kong 	&& chmod -R g=u /usr/local/kong
# Wed, 05 Feb 2020 23:33:02 GMT
USER kong
# Wed, 05 Feb 2020 23:33:02 GMT
COPY file:d4cc11e4d968fd7df92b7b157746b27dc40d08cd20ca769e15cffc687cea9b5c in /docker-entrypoint.sh 
# Wed, 05 Feb 2020 23:33:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2020 23:33:02 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Feb 2020 23:33:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2020 23:33:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0519344698532b61d589f23f1f1283696c4aea5a0bc98f0723c5804873560`  
		Last Modified: Wed, 05 Feb 2020 23:35:01 GMT  
		Size: 6.6 MB (6569287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc04f4753e273e19140c3ee4196ca25937a59f6d3c6efeaba34496f71306fff`  
		Last Modified: Wed, 05 Feb 2020 23:35:11 GMT  
		Size: 75.9 MB (75878730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd763b619dccf9d7c6e7da2acb606b0bbabc1660ef956266ec9d22d20e224b20`  
		Last Modified: Wed, 05 Feb 2020 23:34:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
