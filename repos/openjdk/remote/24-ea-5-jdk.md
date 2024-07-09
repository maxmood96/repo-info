## `openjdk:24-ea-5-jdk`

```console
$ docker pull openjdk@sha256:ff03d0f1fa107d79817bc8d1b5bcca81dfc815dc49d0da4a60b87ae5f25370fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-ea-5-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:62ddf43edad1587d2d318a8b38c6590f08216c626837c644b4397f370fb9eb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298242463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aed08e90d8e7f35d02d4976d3b59a1281c5572f902a9a7fe906605de379d03e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f320f4609c78d43ef6d8e1a2359d2a4040505b830301d5c98599f895a0288ce`  
		Last Modified: Mon, 08 Jul 2024 20:56:58 GMT  
		Size: 37.9 MB (37862625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f53be992d36102e38a13e156f9ab4331c37a5ee8ae29fd2bea84ae5a6135f7a`  
		Last Modified: Mon, 08 Jul 2024 20:57:00 GMT  
		Size: 211.4 MB (211386185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-5-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:a6a49e50e9a687cd8c845fe36898508025d299471ea377979072b05aacf9269a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecab36f0d2cea1ed5f967b73b64b3c09395728b700d443948d6cf65d7f1b7132`

```dockerfile
```

-	Layers:
	-	`sha256:5356f07e20e5a0743b6c55d16e73b78939b76400a4d8b276ee5f2e5c9219674f`  
		Last Modified: Mon, 08 Jul 2024 20:56:57 GMT  
		Size: 3.3 MB (3333228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e68b5a7d1dedc201cdd893c203b9953ea5c64926d62fa66f871bb9b21f37de7`  
		Last Modified: Mon, 08 Jul 2024 20:56:57 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-5-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b327aef9274c67d0a50ae3537b41b89d1a45d21f016a4e66e90070c47f6be277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295173420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7fc350b67e950e4a70dbbcd19f334b082bcd33c039eb69e5f1cbf1af40cb22`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090038af1dc654e39101a0e5c1948e4487961717162abcaa289f614004326864`  
		Last Modified: Mon, 08 Jul 2024 20:57:10 GMT  
		Size: 38.3 MB (38256393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227419e67fdf132c6283bb10917ff62a6e7daf642373b953eb1f91311365ab78`  
		Last Modified: Mon, 08 Jul 2024 20:57:13 GMT  
		Size: 209.3 MB (209264261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-5-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:6ba86c69f38cc658a5e85981b238d7dadb55610a87047c534f0d5042899b397d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc7695dd9476a674beb30971dc97cadb05b6ba55805def63a318b5409c1b3e7`

```dockerfile
```

-	Layers:
	-	`sha256:5aea8a20fb388713125d52040f8cd7e3e9562ac3e46b1a398947ed5a480ff541`  
		Last Modified: Mon, 08 Jul 2024 20:57:09 GMT  
		Size: 3.3 MB (3331611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dbe4e76573a75ba292e38b294c0b3acd0d994e21a572953cc5a3b0f4ca5275a`  
		Last Modified: Mon, 08 Jul 2024 20:57:08 GMT  
		Size: 20.0 KB (19978 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-5-jdk` - windows version 10.0.20348.2529; amd64

```console
$ docker pull openjdk@sha256:0efa4058149b59998d6942de27a849e52aa332db20bb6b82b0cb2dada68951e9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325435891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4796a5f5096cc88c7fe1944e0d7b36c26aedd0510b682c2646aa56f6985fd9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Mon, 08 Jul 2024 20:56:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Jul 2024 20:57:36 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:57:36 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 08 Jul 2024 20:57:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:57:43 GMT
ENV JAVA_VERSION=24-ea+5
# Mon, 08 Jul 2024 20:57:43 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_windows-x64_bin.zip
# Mon, 08 Jul 2024 20:57:44 GMT
ENV JAVA_SHA256=6311a1a2de647471859f4eda1f035e7da59a26882c2bc3e456a97e88b9e9647b
# Mon, 08 Jul 2024 20:58:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:58:10 GMT
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
	-	`sha256:f56e6013afe5aad14ae831320fcc1439d2a8c8850cc862490ce4daf86f0ea0f2`  
		Last Modified: Mon, 08 Jul 2024 20:58:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8d818e4212d9524f07bc31fb22eb5943759dac42c8faba8f183d1f847823f8`  
		Last Modified: Mon, 08 Jul 2024 20:58:14 GMT  
		Size: 369.3 KB (369325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d652ef65eb43b7cc75a79bf3ce2cbc5cc502e09a1855f92a5dfd8ddec7a7e6e6`  
		Last Modified: Mon, 08 Jul 2024 20:58:14 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1a00af15309a7e78189abe71742948d05f14a13c0c98166eb85aea63bf5a11`  
		Last Modified: Mon, 08 Jul 2024 20:58:14 GMT  
		Size: 320.3 KB (320270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f12416285128fa398f4ace89455f42afbd3afc34304a3b8d7695e140b670181`  
		Last Modified: Mon, 08 Jul 2024 20:58:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4098926a0cdd237a5638844be108a9150c4e50250c7ac38cb0ca7562980988c7`  
		Last Modified: Mon, 08 Jul 2024 20:58:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:785927fa36ac33800af4f021b9a4bcb9f1256360bcb346210baadc1b3ccd6b49`  
		Last Modified: Mon, 08 Jul 2024 20:58:13 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff02cf044c24869c6f18a6c0345ab59e16c2fc27c914c82b2d83c2b26aa8b76`  
		Last Modified: Mon, 08 Jul 2024 20:58:24 GMT  
		Size: 206.5 MB (206548299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27dfbc167ff30c92ee6604f5d556112f9c248679203ad02bb8fb80930310a02`  
		Last Modified: Mon, 08 Jul 2024 20:58:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-5-jdk` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:9e83892fbb8636b55ec6b81c742f2d3a7d799d4f2e24d1b53b81224bcdec2ece
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428132332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7685361e79ed9a03691c7aff662894b8e5238eeb1c2b9603be8efd9006aca9e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Mon, 08 Jul 2024 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 08 Jul 2024 20:57:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:57:35 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 08 Jul 2024 20:58:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:58:00 GMT
ENV JAVA_VERSION=24-ea+5
# Mon, 08 Jul 2024 20:58:01 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_windows-x64_bin.zip
# Mon, 08 Jul 2024 20:58:02 GMT
ENV JAVA_SHA256=6311a1a2de647471859f4eda1f035e7da59a26882c2bc3e456a97e88b9e9647b
# Mon, 08 Jul 2024 20:58:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 08 Jul 2024 20:58:56 GMT
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
	-	`sha256:03f6032f3b64aecc584eb246371e0dbbf17c90a5b6a5554366fd9235c797bbcc`  
		Last Modified: Mon, 08 Jul 2024 20:59:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17aa3d7d72129f6ef32c7e8454c0e6695ec205efd5e8defb19af35caffeef772`  
		Last Modified: Mon, 08 Jul 2024 20:59:03 GMT  
		Size: 499.9 KB (499931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bf3dbfdd8caccdebcdb432ed731cfc8526995be0a96db5ba97aeaa001ec8d0`  
		Last Modified: Mon, 08 Jul 2024 20:59:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb749df4a0390d04e45fa5901c7dde1bd18500759a7e5fb0d4f9de11baec923`  
		Last Modified: Mon, 08 Jul 2024 20:59:03 GMT  
		Size: 355.0 KB (354967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa9303a7aca9812093b3421f2d68f5732d11c329fb7a77db60a8f598515cd8c`  
		Last Modified: Mon, 08 Jul 2024 20:59:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b256312bb4649dd394ecc2522f2e4e31709961eb24a712b8beb20805df9cfe7`  
		Last Modified: Mon, 08 Jul 2024 20:59:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52485716f5016887a660a380276adfa40a4acc30bbeeb9861b4ce1c4f04fc75`  
		Last Modified: Mon, 08 Jul 2024 20:59:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29eeaf502b9f722fc7866935f8074f375b4f8d3deab2ae41fa18de5aff2eace`  
		Last Modified: Mon, 08 Jul 2024 20:59:11 GMT  
		Size: 206.6 MB (206588484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:310ed6c903e384fecfd8fd76c6669cbd5540347c679c6eaa400441821c5af02e`  
		Last Modified: Mon, 08 Jul 2024 20:59:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
