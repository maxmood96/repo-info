## `openjdk:24-jdk`

```console
$ docker pull openjdk@sha256:8abe91a7be6ad2798ea7fcbe508a8d62a2159ea188bb3aa5634c0d1db9178eee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:9aadef1fdb138330c3e0cf6e7c910891b27feb4aa5efddadc6ff2c9b4120a703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298171618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25da023794f6155919522ef1f467c621ff346e0a3de5ccdc3361149cdcfd2e42`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 29 Jun 2024 00:52:17 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_VERSION=24-ea+4
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='64aa493b28493a2d223626bdad774640cb148b0d52f392b081b2776532a980a0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d0b65f191528ab241b4e238568e52fa7199975b4f4b7badcf58a279b1fac426'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaa553e046eeac03f941d9c5aeff3b502c3f1ce8778bbcd065d0a8d6fb57b34`  
		Last Modified: Tue, 02 Jul 2024 00:57:35 GMT  
		Size: 37.9 MB (37862476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aa169db96cd047ff2618e1d057812c40fd64b9b3b13af4826f43b8ddb53fb3`  
		Last Modified: Tue, 02 Jul 2024 00:57:38 GMT  
		Size: 211.3 MB (211315489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:bcf7b9a06bebfae8144b2c7dc8d17c82161e89416dcc6aa9dd5b8005c091e403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ec84814c514157837261d3006b9e2c44e595c06e689bd2c3eb489edd846c8e`

```dockerfile
```

-	Layers:
	-	`sha256:d5665a463a3e0270a9af9fe5b51ae990a479d7fe58cb929e073b8534eee8ce42`  
		Last Modified: Tue, 02 Jul 2024 00:57:35 GMT  
		Size: 3.3 MB (3333228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae88bc31ebbad7d65a632a331b1c210135613d4395f8f95e1ace39608ff7a6b`  
		Last Modified: Tue, 02 Jul 2024 00:57:35 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f51ceb413bb0ea2e42ed05e9364ecb4c694cf6206e3ec14080c277f4449be679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295121336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c9723862e12d7e48d4f7a2d2dcdabdabf7be1f51c99f6bcbe3bf6ee40f669a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 18:52:10 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 18:52:10 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 21 Jun 2024 18:52:10 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:52:10 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_VERSION=24-ea+3
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='dad750c864049dba95a01fa89ad1c52c3b702ba87c3c865e5e64fa624f9e3de0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='4a5515c226db56008676461bef7443163ccfe369415342136b8d9691ecd5130b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e03e86442d91879ee632bd4444507fcf4dadd66cc8c2b8458e11db03d0883c`  
		Last Modified: Fri, 21 Jun 2024 20:58:16 GMT  
		Size: 38.3 MB (38256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5843006ae468b96ecdee72b763966993d99590f92f2505d70cc86455c0492b`  
		Last Modified: Sat, 22 Jun 2024 06:16:10 GMT  
		Size: 209.2 MB (209212140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f9d8d4e16c951771d8579b5c6318d1d153b195a53302e9a85264a1bec58913c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d021404f19396d134b8296a538f74547a178fb135d45881f073cd7a567097cf`

```dockerfile
```

-	Layers:
	-	`sha256:1e6cab75b0a4adb5e1e825036613b5cb85ee9e53d2e224e952088502718b2328`  
		Last Modified: Sat, 22 Jun 2024 06:16:05 GMT  
		Size: 3.3 MB (3331611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25da4184b2b06c5043021db97f0ed5c6d3a94d213debe879a239edbf6ae1b800`  
		Last Modified: Sat, 22 Jun 2024 06:16:04 GMT  
		Size: 20.0 KB (19978 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk` - windows version 10.0.20348.2529; amd64

```console
$ docker pull openjdk@sha256:7918e7346b562564acbd4003b27786de6c0b72229c4dd1f76a271953685ee4f8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325404296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fcc868e891d4def65badeb26d80ce1d40ba7ae405151af2d360994b987bd34`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Tue, 02 Jul 2024 00:57:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 00:57:59 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:57:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 02 Jul 2024 00:58:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:58:06 GMT
ENV JAVA_VERSION=24-ea+4
# Tue, 02 Jul 2024 00:58:06 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_windows-x64_bin.zip
# Tue, 02 Jul 2024 00:58:07 GMT
ENV JAVA_SHA256=49def475d4ac8b16fc13e9f43cb195b1da28c70cbfa438466e25f7b82c5c55a2
# Tue, 02 Jul 2024 00:58:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:58:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78023868517c9e90cd1a2da57a94d15b051ec6e346b01dc6db1422b9a42efe46`  
		Last Modified: Tue, 02 Jul 2024 00:58:39 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5569bc9a87b1ba1cdefcec68115c4739eabeab66f7766c2bbd5037eee60598f`  
		Last Modified: Tue, 02 Jul 2024 00:58:39 GMT  
		Size: 359.7 KB (359696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6780b70e7c9a26687fb9cbb876d11dc82bf99a0016852dfce87b7709fd5c9f9`  
		Last Modified: Tue, 02 Jul 2024 00:58:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c380a3d2cb1adee65a90fb600092d0786df1cb4dbfcf4096ca431be8949afc1`  
		Last Modified: Tue, 02 Jul 2024 00:58:39 GMT  
		Size: 345.6 KB (345562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9ca61ef1b1da104241c922ec429f6c70cdfde7947957e5999c1854772d9da0`  
		Last Modified: Tue, 02 Jul 2024 00:58:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f9966908c26c02ef9cca1c142c3847badebd914e3d05f8fc4b6cecb0c9226`  
		Last Modified: Tue, 02 Jul 2024 00:58:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a69efd113708e0e938933a3caf1e72a2a78ee9fd6e1dc43f2c30c1b2073119b`  
		Last Modified: Tue, 02 Jul 2024 00:58:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2035dc4544631d55c9769410ea995617440af3d55307e42059e1568b16e9d6a3`  
		Last Modified: Tue, 02 Jul 2024 00:58:48 GMT  
		Size: 206.5 MB (206500984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f966edd9ceeac2ac401fc189601209421fa0cee01095d974d0088d623da5d76a`  
		Last Modified: Tue, 02 Jul 2024 00:58:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-jdk` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:07b613582ef426417ddcfa25f4c74ed0898b511ffb9b32238cf020a93c58bbf9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428017063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94eebeaf6a796ef8a1df3d090e5ed5d9eaa6b547d823c9a8e19b3095109f926f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Tue, 02 Jul 2024 00:57:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 00:59:10 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:59:10 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 02 Jul 2024 00:59:35 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jul 2024 00:59:35 GMT
ENV JAVA_VERSION=24-ea+4
# Tue, 02 Jul 2024 00:59:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_windows-x64_bin.zip
# Tue, 02 Jul 2024 00:59:36 GMT
ENV JAVA_SHA256=49def475d4ac8b16fc13e9f43cb195b1da28c70cbfa438466e25f7b82c5c55a2
# Tue, 02 Jul 2024 01:00:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576b05aa6cfc9b0f90b35036fbca23f1b4521dbfd96b5c17a270dbf39faca1c4`  
		Last Modified: Tue, 02 Jul 2024 01:00:27 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2af6637cad12d78a155dba53b7254da1061f4561c75a67b4a55e81244c3599b`  
		Last Modified: Tue, 02 Jul 2024 01:00:28 GMT  
		Size: 486.6 KB (486574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa1a1ae88453744b49872a2dd531b2f566c498fddebc4e4ddfa7da6cb9077ac`  
		Last Modified: Tue, 02 Jul 2024 01:00:27 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b7e65ebf9e738d4b179cb861461264492f4a6b5266408e72f40eefc02d00e`  
		Last Modified: Tue, 02 Jul 2024 01:00:28 GMT  
		Size: 341.3 KB (341254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915a01238d030449bfe898b374723db1bbdddef91ca5a158bc2a4b51018aa6e4`  
		Last Modified: Tue, 02 Jul 2024 01:00:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac799793af619f2e0fd4d5aa582872d04ed31db4e3a7c08193d4fd4b6009393`  
		Last Modified: Tue, 02 Jul 2024 01:00:26 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc81c8d8cab25cfa605502f99b4a6e8f1d4bbf2b7a413b52ee2bbc17f530165`  
		Last Modified: Tue, 02 Jul 2024 01:00:26 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3dd44a16534fba5d6ad31011f1c8429f708f6ecfcd86158367a1d70ec8953b`  
		Last Modified: Tue, 02 Jul 2024 01:00:37 GMT  
		Size: 206.5 MB (206500271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738d6df23d3bfa1cdc449f4d160e2b734f552a61ff657f292186d7226298c300`  
		Last Modified: Tue, 02 Jul 2024 01:00:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
