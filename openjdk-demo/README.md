# Java Swing Examples snap

This project create a snap for the Java Swing example applications.

## Current State

Crashes on startup because of snappy desktop integration issues (system fonts, fontconfig, etc)
```
Jun 03, 2016 6:24:52 PM FileChooserDemo main
SEVERE: null
java.lang.reflect.InvocationTargetException
	at java.awt.EventQueue.invokeAndWait(EventQueue.java:1321)
	at java.awt.EventQueue.invokeAndWait(EventQueue.java:1296)
	at javax.swing.SwingUtilities.invokeAndWait(SwingUtilities.java:1348)
	at FileChooserDemo.main(FileChooserDemo.java:796)
Caused by: java.lang.NullPointerException
	at sun.awt.FontConfiguration.getVersion(FontConfiguration.java:1264)
	at sun.awt.FontConfiguration.readFontConfigFile(FontConfiguration.java:219)
	at sun.awt.FontConfiguration.init(FontConfiguration.java:107)
	at sun.awt.X11FontManager.createFontConfiguration(X11FontManager.java:774)
	at sun.font.SunFontManager$2.run(SunFontManager.java:431)
	at java.security.AccessController.doPrivileged(Native Method)
	at sun.font.SunFontManager.<init>(SunFontManager.java:376)
	at sun.awt.FcFontManager.<init>(FcFontManager.java:35)
	at sun.awt.X11FontManager.<init>(X11FontManager.java:57)
	at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)
	at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62)
	at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45)
	at java.lang.reflect.Constructor.newInstance(Constructor.java:423)
	at java.lang.Class.newInstance(Class.java:442)
	at sun.font.FontManagerFactory$1.run(FontManagerFactory.java:83)
	at java.security.AccessController.doPrivileged(Native Method)
	at sun.font.FontManagerFactory.getInstance(FontManagerFactory.java:74)
	at sun.font.SunFontManager.getInstance(SunFontManager.java:250)
	at sun.font.FontDesignMetrics.getMetrics(FontDesignMetrics.java:264)
	at sun.swing.SwingUtilities2.getFontMetrics(SwingUtilities2.java:1113)
	at javax.swing.JComponent.getFontMetrics(JComponent.java:1626)
	at javax.swing.plaf.basic.BasicLabelUI.getPreferredSize(BasicLabelUI.java:227)
	at javax.swing.JComponent.getPreferredSize(JComponent.java:1662)
	at javax.swing.plaf.basic.BasicListUI.updateLayoutState(BasicListUI.java:1363)
	at javax.swing.plaf.basic.BasicListUI.maybeUpdateLayoutState(BasicListUI.java:1311)
	at javax.swing.plaf.basic.BasicListUI$Handler.valueChanged(BasicListUI.java:2623)
	at javax.swing.DefaultListSelectionModel.fireValueChanged(DefaultListSelectionModel.java:184)
	at javax.swing.DefaultListSelectionModel.fireValueChanged(DefaultListSelectionModel.java:164)
	at javax.swing.DefaultListSelectionModel.fireValueChanged(DefaultListSelectionModel.java:211)
	at javax.swing.DefaultListSelectionModel.changeSelection(DefaultListSelectionModel.java:405)
	at javax.swing.DefaultListSelectionModel.changeSelection(DefaultListSelectionModel.java:415)
	at javax.swing.DefaultListSelectionModel.setSelectionInterval(DefaultListSelectionModel.java:459)
	at javax.swing.JList.setSelectedIndex(JList.java:2210)
	at javax.swing.plaf.basic.BasicComboPopup.setListSelection(BasicComboPopup.java:1168)
	at javax.swing.plaf.basic.BasicComboPopup.access$300(BasicComboPopup.java:63)
	at javax.swing.plaf.basic.BasicComboPopup$Handler.itemStateChanged(BasicComboPopup.java:999)
	at javax.swing.JComboBox.fireItemStateChanged(JComboBox.java:1223)
	at javax.swing.JComboBox.selectedItemChanged(JComboBox.java:1280)
	at javax.swing.JComboBox.contentsChanged(JComboBox.java:1330)
	at javax.swing.AbstractListModel.fireContentsChanged(AbstractListModel.java:118)
	at javax.swing.plaf.metal.MetalFileChooserUI$FilterComboBoxModel.propertyChange(MetalFileChooserUI.java:1078)
	at java.beans.PropertyChangeSupport.fire(PropertyChangeSupport.java:335)
	at java.beans.PropertyChangeSupport.firePropertyChange(PropertyChangeSupport.java:327)
	at java.beans.PropertyChangeSupport.firePropertyChange(PropertyChangeSupport.java:263)
	at java.awt.Component.firePropertyChange(Component.java:8430)
	at javax.swing.JFileChooser.setFileFilter(JFileChooser.java:1473)
	at javax.swing.JFileChooser.addChoosableFileFilter(JFileChooser.java:1151)
	at javax.swing.JFileChooser.updateUI(JFileChooser.java:1839)
	at javax.swing.JFileChooser.setup(JFileChooser.java:371)
	at javax.swing.JFileChooser.<init>(JFileChooser.java:343)
	at javax.swing.JFileChooser.<init>(JFileChooser.java:296)
	at FileChooserDemo.<init>(FileChooserDemo.java:177)
	at FileChooserDemo$2.run(FileChooserDemo.java:816)
	at java.awt.event.InvocationEvent.dispatch(InvocationEvent.java:301)
	at java.awt.EventQueue.dispatchEventImpl(EventQueue.java:756)
	at java.awt.EventQueue.access$500(EventQueue.java:97)
	at java.awt.EventQueue$3.run(EventQueue.java:709)
	at java.awt.EventQueue$3.run(EventQueue.java:703)
	at java.security.AccessController.doPrivileged(Native Method)
	at java.security.ProtectionDomain$JavaSecurityAccessImpl.doIntersectionPrivilege(ProtectionDomain.java:76)
	at java.awt.EventQueue.dispatchEvent(EventQueue.java:726)
	at java.awt.EventDispatchThread.pumpOneEventForFilters(EventDispatchThread.java:201)
	at java.awt.EventDispatchThread.pumpEventsForFilter(EventDispatchThread.java:116)
	at java.awt.EventDispatchThread.pumpEventsForHierarchy(EventDispatchThread.java:105)
	at java.awt.EventDispatchThread.pumpEvents(EventDispatchThread.java:101)
	at java.awt.EventDispatchThread.pumpEvents(EventDispatchThread.java:93)
	at java.awt.EventDispatchThread.run(EventDispatchThread.java:82)
```