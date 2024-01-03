## WPF - Custom Control 

/* 
8.1 Create a form to get customer details such as name, address,contact, pincode. *(without using custom control for text box)
*/ 
### MainWindow.xaml
```html
<Window x:Class="WpfApp1.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:WpfApp1"
        mc:Ignorable="d"
        Title="MainWindow" Height="300" Width="300">
    <Grid>
        <Grid.RowDefinitions >
            <RowDefinition />
            <RowDefinition />
            <RowDefinition />
            <RowDefinition />
        </Grid.RowDefinitions>
        <TextBox Grid.Row="0" Height="30" Width="250" Text="Enter Name"     HorizontalAlignment="Center" VerticalAlignment="Center"/>
        <TextBox Grid.Row="1" Height="30" Width="250" Text="Enter Address"  HorizontalAlignment="Center" VerticalAlignment="Center"/>
        <TextBox Grid.Row="2" Height="30" Width="250" Text="Enter Contact"  HorizontalAlignment="Center" VerticalAlignment="Center"/>
        <TextBox Grid.Row="3" Height="30" Width="250" Text="Enter pin code" HorizontalAlignment="Center" VerticalAlignment="Center" />
    </Grid>
</Window>

```
---

/* 
8.2 Create a custom text box .
*/   
Directory Structure -
![image](https://github.com/codewithheeren/.Net/assets/87074236/f17faccd-ee23-4081-8adc-6190f481f36e)

### ReusableTextBox.xaml
```html
<UserControl x:Class="WpfApp1.view.UserControls.ReusableTextBox"
             xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
             xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
             xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006" 
             xmlns:d="http://schemas.microsoft.com/expression/blend/2008" 
             xmlns:local="clr-namespace:WpfApp1.view.UserControls"
             mc:Ignorable="d" 
             d:DesignHeight="40" d:DesignWidth="250">
    <Grid>
        <TextBox x:Name="txtInput"  VerticalAlignment="Center" FontSize="18" FontWeight="Light" 
                 HorizontalAlignment="Left" Width="250" />
        <TextBlock x:Name="tbPlaceholder"  Text="Enter Value" FontSize="18" FontWeight="Light"
                   VerticalAlignment="Center" Foreground="LightGray" Margin="5,0,0,0"/>
        <Button x:Name="btnClear" Width="30" HorizontalAlignment="Right" Content="X" FontSize="20"
                FontWeight="Medium" Background="Transparent" Foreground="LightGray" 
                BorderThickness="0"/>
    </Grid>
</UserControl>

```
---